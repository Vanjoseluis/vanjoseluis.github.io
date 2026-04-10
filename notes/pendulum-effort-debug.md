[Home](../index.md)

# Debugging a Non‑Deterministic Regression in pendulum_effort_test
In early March 2026, a previously stable test in gz_ros2_control — pendulum_effort_test — began failing intermittently on Rolling.
This note documents the debugging process, the root cause, and the final fix that was merged and backported across four ROS 2 distributions.

---
## 🧩 1. Symptoms: A deterministic test becomes flaky
The upstream test began producing inconsistent results:
```
ISSUE 801 — pendulum_effort_test (Rolling)
1.  expected 1.57, got 1.36  failed
2.  expected 1.57, got 1.54  failed
3.  expected 1.57, got 1.57  passed
4.  expected 1.57, got 1.55  failed
5.  expected 1.57, got 1.40  failed
6.  expected 1.57, got 1.41  failed
7.  expected 1.57, got 1.37  failed
8.  expected 1.57, got 1.42  failed
9.  expected 1.57, got 1.09  failed
10. expected 1.57, got 1.31  failed
11. expected 1.57, got 1.54  failed
```
Additional symptoms appeared:
```
malloc.c:2599 (sysmalloc): assertion failed

Timeouts contacting /controller_manager/list_controllers (50s)
```
However, the same test on the previous Rolling version behaved consistently:
```
PR 765 branch — previous Rolling
1–7: all passed
8: expected 1.57, got 1.46  failed
9–11: all passed
```
This strongly suggested a regression introduced upstream, not a problem in the test itself.

## 🧪 2. Reproducing the issue
To ensure reproducibility, each commit was tested with:
```
colcon test --packages-select gz_ros2_control_tests \
  --ctest-args -R pendulum_effort_test \
  --repeat-until-fail 10 \
  --event-handlers console_direct+
```
This allowed distinguishing:
- deterministic failures
- non‑deterministic behavior
- timing‑related issues

## 🔍 3. Git bisect: isolating the regression
A full bisect was performed:
```
git bisect start
git bisect bad
git bisect good 5c63578
```
For each commit:
```
source ~/ws_ros2_control/install/setup.bash
colcon build --packages-select gz_ros2_control gz_ros2_control_tests
colcon test ...
git bisect good|bad
```
**Results**:
```
PR #790 → 20/20 passed → good
PR #800 → 10/10 passed → good
```
The first failing commit was:
```
8f6caa0de307bfc9c7a4e87784f8bdf7bd49c6af
Author: Alejandro Hernández Cordero
Precompute interface names (#789)
```
## 🧨 4. Root cause: a timing change that introduced a race condition
Inside gz_ros2_control_plugin.cpp, the initialization wait time changed from:
```
cpp
std::this_thread::sleep_for(std::chrono::microseconds(2000000));
```
to:
```
cpp
std::this_thread::sleep_for(std::chrono::milliseconds(200));
```
But:
*2000000 microseconds = 2000 ms*

The new value was 200 ms, a 10× reduction

This caused:
- the Resource Manager to initialize after the simulation started
- controllers to load inconsistently
- non‑deterministic pendulum behavior
- flaky test results
- occasional glibc allocation failures
- service timeouts
- A classic race condition triggered by insufficient initialization time.

## 🛠️ 5. The fix
Restoring the original wait time solved the issue:
```
cpp
std::this_thread::sleep_for(std::chrono::milliseconds(2000));
```
Validation:
```
10/10 deterministic passes
```
- No glibc errors
- No controller_manager timeouts
- Stable behavior across runs

A PR ([#809](https://github.com/ros-controls/gz_ros2_control/pull/809)) was opened with the fix.
Alejandro Hernández Cordero reviewed, merged, and backported it to Humble, Jazzy, Kilted, and Rolling.

## 📚 6. Lessons learned
♠️ Debugging non‑deterministic behavior
Requires controlled experiments, repeated runs, and careful observation.

♦️ Using git bisect effectively
Essential for isolating regressions in large codebases.

♣️ Timing matters
Small changes in initialization order can create subtle race conditions.

♥️ Open‑source collaboration
The fix now ships in four ROS 2 distros thanks to fast maintainer feedback.

🔗 Related PRs and issues
Issue: [https://github.com/ros-controls/gz_ros2_control/issues/801](https://github.com/ros-controls/gz_ros2_control/issues/801) 

Fix PR: [https://github.com/ros-controls/gz_ros2_control/pull/809](https://github.com/ros-controls/gz_ros2_control/pull/809)

Regression commit: [#789](https://github.com/ros-controls/gz_ros2_control/pull/789)
