## 🔧 Open Source Contributions

### ros-controls / gz_ros2_control

- My first contribution was adding a new integration test and “initial_value checker” to gz_ros2_control (PR [#765](https://github.com/ros-controls/gz_ros2_control/pull/765)), later backported manually to Jazzy (PR [#781](https://github.com/ros-controls/gz_ros2_control/pull/781)). I am currently working on the Humble and Kilted distros.  
- Investigated intermittent failures on ROS 2 Rolling (Issue [#801](https://github.com/ros-controls/gz_ros2_control/issues/801)); after rebuilding Rolling and comparing with older branches, I identified that the problem came from an upstream regression, not from the test. The fix was merged and backported with PR [#809](https://github.com/ros-controls/gz_ros2_control/pull/809).  
- Added additional long‑lasting tests (pendulum_position and gripper) in PR [#814](https://github.com/ros-controls/gz_ros2_control/pull/814), increasing demo coverage from 5 to 9.

