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

# 🎓 Academic Projects

A collection of university and training projects focused on robotics, automation, digital electronics, and applied systems engineering.

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

# 🧰 Personal Projects

These projects focus on developer tooling, deterministic testing, simulation performance, and ecosystem analysis for ROS 2.

---

## 🔍 ros2-debug-assistant

Page:  
[ros2-debug-assistant](https://github.com/Vanjoseluis/vanjoseluis.github.io/blob/main/projects/ros2-debug-assistant.md)  
Repository:  
[https://github.com/Vanjoseluis/ros2-debug-assistant](https://github.com/Vanjoseluis/ros2-debug-assistant)

Structural analysis and automatic fixes for ROS 2 packages.  
Detects formatting issues, missing dependencies, CMake problems, and common pitfalls — and suggests or applies fixes automatically.

---

## 🧪 autotest (planned)

Deterministic CI for controllers and simulation.  
A testing framework for reproducible controller validation, multi‑run consistency checks, and automated regression detection in `ros2_control` and `gz_ros2_control`.

👉 Project page coming soon

---

## 🏎️ fastzebo (planned)

A modern, ROS‑native fast simulation backend.  
Explores faster, more deterministic simulation pipelines for ROS 2, bridging traditional simulators and high‑performance physics engines.

👉 Project page coming soon

---

## 🕸️ ecosystem analyzer (TFG)

PR/Issue conflict graph for ros‑controls maintainers.  
Undergraduate thesis project analyzing repository history to detect conflicting PRs, dependency chains, and structural risks in the ros‑controls ecosystem.

👉 Project page coming soon

---

# 📝 Technical Notes

Short write‑ups on debugging, tests, controller_manager internals, and lessons learned while contributing to Open Source.

👉 [Notes](notes/)

---

# 📬 Contact

- GitHub: [@Vanjoseluis](https://github.com/Vanjoseluis)  
- LinkedIn: https://www.linkedin.com/in/josé-luis-pérez-martín
