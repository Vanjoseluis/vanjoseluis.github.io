[Home](../index.md)

# José Luis Pérez Martín  
Robotics & Open‑Source Developer

I am a robotics student at the University of Málaga and an active contributor to the ROS 2 ecosystem, especially **ros-controls** and **gz_ros2_control**.  
My work focuses on controller infrastructure, testing, debugging, and reproducible robotics workflows. I enjoy understanding systems deeply, improving reliability, and contributing upstream through clear, incremental pull requests.

This site collects my open‑source contributions, technical notes, and my work toward the **Google Summer of Code 2026** project:  
**Mission Control for ros2_control**.

---

## 🔧 Open‑Source Contributions

I contribute regularly to the ROS 2 control stack, including:

- `ros-controls/ros2_control`
- `ros-controls/gz_ros2_control`
- related testing and simulation tools

See the full list here:  
👉 [Contributions](contributions.md)

---

## 🚀 GSoC 2026 — Mission Control for ros2_control

I am preparing a proposal to develop a mission‑control component for ros2_control, focusing on:

- dynamic introspection of controllers  
- standardized status publishing  
- safe lifecycle orchestration  
- reproducible multi‑robot benchmarks  

Details, design notes, and the 12‑week plan:  
👉 [GSoC 2026](gsoc-2026.md)

---

# 🛠️ Projects

This section collects the tools, academic work, and infrastructure I am building to improve reproducibility, introspection, and reliability in ROS 2 development.  
Each project reflects my focus on systems engineering, debugging, testing, and upstream contributions to the ROS 2 control ecosystem.

---

# 🧰 Personal Projects

These projects focus on developer tooling, deterministic testing, simulation performance, and ecosystem analysis for ROS 2.  
They complement my upstream contributions to ros-controls and my academic work in robotics, automation, and digital systems.

---

## 🔍 ros2-debug-assistant

Page:  
[ros2-debug-assistant](https://github.com/Vanjoseluis/vanjoseluis.github.io/blob/main/projects/ros2-debug-assistant.md)

Repository:  
[https://github.com/Vanjoseluis/ros2-debug-assistant](https://github.com/Vanjoseluis/ros2-debug-assistant)

**Structural analysis and automatic fixes for ROS 2 packages.**

`ros2-debug-assistant` is a static analysis tool that detects formatting inconsistencies, linter errors, missing dependencies, and CMake/manifest misconfigurations **before build time**.  
It focuses on the *ecosystem around your code* — package metadata, build tooling, and structure — rather than runtime logic.

**Key features:**
- Detects trailing whitespace, mixed tabs/spaces, indentation inconsistencies, overly long lines.  
- Parses package structure to detect missing dependencies and common manifest issues.  
- Identifies CMake configuration problems and ament_lint pitfalls.  
- Provides **clear, human‑readable diagnostics**.

**Automatic fix engine:**
- Whitespace cleanup  
- Tab → space normalization  
- Indentation normalization  
- Interactive mode:  

**Architecture:**
ros2-debug-assistant
│
├── cli.py          # Command-line interface
├── analyzer.py     # Static analysis of files and package structure
├── fixer.py        # Automatic corrections and formatting fixes
└── utils.py        # Shared helpers


**Roadmap:**
- ament_lint integration  
- dependency validation  
- CMakeLists.txt structure analysis  
- launch/test diagnostics  
- VSCode extension with “Accept fix” UI  

---

## 🧪 autotest (planned)

**Deterministic CI for controllers and simulation.**

A testing framework for reproducible controller validation, multi‑run consistency checks, and automated regression detection in `ros2_control` and `gz_ros2_control`.

**Goals:**
- Detect nondeterministic startup behavior.  
- Identify physics‑induced jitter and timing drift.  
- Provide multi‑run reproducibility metrics.  
- Integrate with CI pipelines to catch regressions *before merging*.  

**Focus areas:**
- Deterministic behavior  
- Timing stability  
- Cross‑distro reproducibility  
- Automated regression detection  

👉 Project page coming soon

---

## 🏎️ fastzebo (planned)

**A modern, ROS‑native fast simulation backend.**

A long‑term project exploring faster, more deterministic simulation pipelines for ROS 2, bridging the gap between traditional simulators and high‑performance physics engines.

**Goals:**
- Improved startup determinism  
- Reduced physics jitter  
- Optimized sensor/physics loops  
- Deterministic state capture  
- High‑performance simulation for robotics research  

**Vision:**
A conceptual foundation for future research in simulation performance and real‑time robotics.

👉 Project page coming soon

---

## 🕸️ ecosystem analyzer (TFG)

**PR/Issue conflict graph for ros-controls maintainers.**

Undergraduate thesis project analyzing repository history to detect conflicting pull requests, dependency chains, and structural risks in the ros-controls ecosystem.

**Key ideas:**
- Graph‑based model of PR interactions  
- Detection of hidden conflicts and risky merges  
- Analysis of backports, regressions, and distro divergence  
- Support maintainers with structural insights into the ecosystem  

**Impact:**
Helps maintainers identify architectural bottlenecks and reduce integration risk.

👉 Project page coming soon

---

# 🎓 Academic Projects

🎓 [Academic Projects](https://github.com/Vanjoseluis/vanjoseluis.github.io/blob/main/projects/academic-projects.md)

A collection of university projects focused on robotics, algorithms, systems engineering, and applied software development.  
These projects complement my personal tools and open‑source contributions.

👉 Repository:  
[https://github.com/Vanjoseluis/Academic_Projects](https://github.com/Vanjoseluis/Academic_Projects)

---

## 🏭 GEMMA Based Control System for FMS 205 (TwinCAT 3)

**University of Málaga — School of Industrial Engineering (June 2025)**  
Repository:  
[https://github.com/Vanjoseluis/Academic_Projects/tree/main/GEMMA_FMS205](https://github.com/Vanjoseluis/Academic_Projects/tree/main/GEMMA_FMS205)

Designed and implemented the complete control logic for the FMS 205 flexible manufacturing station using TwinCAT 3 and a fully modular PLC architecture.  
The system integrates pneumatic actuators, industrial sensors, encoder‑based measurement, and a full HMI, following the GEMMA operational framework for safe and deterministic behavior.

**Key contributions:**
- Modular PLC architecture (MAIN → Station Controller → Coordinator → Task FBs) using ST and SFC.  
- GEMMA‑based operational modes: startup, shutdown, fault handling, recovery.  
- Five independent SFC task modules with deterministic synchronization (Ready/Execute/Done/Ack).  
- Integration of inductive, capacitive, photoelectric sensors, linear encoder, cylinders, vacuum ejector, conveyor.  
- Full TwinCAT HMI with mode selection, counters, and real‑time visualization.  
- Professional documentation: I/O mapping, module descriptions, sequence diagrams, control flow.

**Impact:**
- Clean, scalable, industry‑style PLC architecture.  
- Deterministic task coordination and safe operation.  
- Demonstrated strong capability in industrial automation and control logic design.

---

## 🐧 Bash‑Based Naive Obstacle Avoider for ROS 2 (July 2025)

Repository:  
[https://github.com/Vanjoseluis/Academic_Projects/tree/main/Linux_TheConstruct_Project](https://github.com/Vanjoseluis/Academic_Projects/tree/main/Linux_TheConstruct_Project)

A lightweight obstacle avoidance system built entirely with Bash scripting and ROS 2 parameters.  
Uses LaserScan, odometry, and IMU data to drive robot motion through `cmd_vel` parameters — an educational alternative to Python/C++ nodes.

**Features:**
- Naive obstacle avoidance using front/left/right distance thresholds.  
- Real‑time decision making via infinite Bash loops.  
- Live telemetry printing (position, orientation, IMU, velocity).  
- Modular design using `robot_functions.bash`.

**Requirements:**
- ROS 2 Humble (or compatible).  
- Robot exposing `/robot_interface` parameters.  
- `ros2 param` CLI.  
- `bc` installed for float comparison.

---

## 🐍 ROS 2 Obstacle Avoider in Python (July 2025)

Repository:  
[https://github.com/Vanjoseluis/Academic_Projects/tree/main/Python_TurtleBot_Project](https://github.com/Vanjoseluis/Academic_Projects/tree/main/Python_TurtleBot_Project)

A ROS 2 node written in Python implementing reactive obstacle avoidance using LaserScan, IMU, odometry, and Twist commands.  
Designed for TurtleBot‑like robots, providing a clean and extensible baseline for navigation and behavior‑based control.

**Features:**
- Obstacle avoidance using frontal sectors (left, center, right).  
- Orientation tracking (yaw).  
- Reactive algorithm: turn or move forward based on distance readings.  
- Easily extendable logic for navigation, mapping, or behavior trees.

---

## 🔌 Digital Electronics Project — Combinational & Sequential System Design (VHDL, FPGA)

**University of Málaga — School of Industrial Engineering (May 2025)**  
Repository:  
[https://github.com/Vanjoseluis/Academic_Projects/tree/main/Digital_Electronics](https://github.com/Vanjoseluis/Academic_Projects/tree/main/Digital_Electronics)

Designed and implemented two complementary digital systems using VHDL, combinational logic, and sequential finite state machines.  
Includes analytical derivation, Karnaugh minimization, state machine modeling, schematic synthesis, simulation, and FPGA deployment on a Nexys3 board.

**Subsystems:**
- **Electronic Voting System** — combinational + sequential architecture for vote counting and evaluation.  
- **Secure Door Control FSM** — deterministic state machine with safety constraints and timeout logic.

**Key contributions:**
- Full combinational subsystem: vote counter, seven‑segment controller, majority evaluator.  
- Truth tables + Karnaugh maps for 256 combinations.  
- Sequential subsystem (Reg_Vot) as Moore FSM.  
- Supporting modules: ENA_GEN, Puls_On_Off, Ctrl_Leds.  
- Secure door FSM with 5 states (A–E), error handling, deterministic transitions.  
- Structured VHDL testbenches and FPGA deployment.  
- Simulation chronograms and timing validation.

---

# 📝 Technical Notes

Short write‑ups on debugging, tests, controller_manager internals, and lessons learned while contributing to Open Source.

👉 [Notes](notes/)

---

# 📬 Contact

- GitHub: [@Vanjoseluis](https://github.com/Vanjoseluis)  
- LinkedIn: https://www.linkedin.com/in/josé-luis-pérez-martín
