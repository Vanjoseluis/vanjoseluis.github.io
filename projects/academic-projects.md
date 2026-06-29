# 🎓 Academic Projects

This page collects selected academic work completed during my studies at the University of Málaga.  
These projects focus on robotics, automation, digital electronics, systems engineering, and applied software development.

---

## 📚 Repository  
All academic projects are available here:  
https://github.com/Vanjoseluis/Academic_Projects

---

# 🧩 Categories

### Robotics & Control
Work involving:
- reactive navigation  
- sensor‑driven control  
- ROS 2 experimentation  
- industrial automation (TwinCAT 3, GEMMA, SFC/GRAFCET)

### Software Engineering
Projects covering:
- modular architectures  
- reproducible workflows  
- testing and validation  
- CLI‑based robotics tooling

### Digital Electronics & Computation
Work involving:
- VHDL design  
- combinational/sequential logic  
- FSM modeling  
- FPGA deployment  
- analytical derivation and timing analysis

More detailed write‑ups will be added over time.

---

# 🏭 GEMMA Based Control System for FMS 205 (TwinCAT 3)

**University of Málaga — School of Industrial Engineering (June 2025)**  
Repository:  
https://github.com/Vanjoseluis/Academic_Projects/tree/main/GEMMA_FMS205

A complete control system for the FMS 205 flexible manufacturing station, built using **TwinCAT 3**, **Structured Text**, **SFC/GRAFCET**, and **GEMMA methodology**.  
The project integrates real industrial hardware: pneumatic actuators, inductive/capacitive/photoelectric sensors, a linear encoder, and a conveyor system.

### 🔧 Technologies  
TwinCAT 3 · Beckhoff PLCs · ST · EtherCAT · Pneumatics · SFC/GRAFCET · HMI design

### ⭐ Key Contributions
- Modular PLC architecture (MAIN → Station Controller → Coordinator → Task FBs).  
- GEMMA‑based operational modes: startup, shutdown, fault handling, recovery.  
- Five SFC task modules with deterministic Ready/Execute/Done/Ack synchronization.  
- Full TwinCAT HMI with mode selection, counters, and real‑time visualization.  
- Professional documentation: I/O mapping, module descriptions, sequence diagrams, control flow.

### 📈 Impact
- Clean, scalable, industry‑style PLC architecture.  
- Deterministic task coordination and safe operation.  
- Demonstrated strong capability in industrial automation and control logic design.

---

# 🐧 Bash‑Based Naive Obstacle Avoider for ROS 2

**The Construct (July 2025)**  
Repository:  
https://github.com/Vanjoseluis/Academic_Projects/tree/main/Linux_TheConstruct_Project

A lightweight obstacle avoidance system implemented **entirely in Bash**, using ROS 2 parameters and CLI tools.  
It reads LaserScan, IMU, and odometry values to drive robot motion through `cmd_vel` parameters.

### 🔧 Features
- Sector‑based obstacle avoidance (front/left/right).  
- Real‑time decision loops using Bash.  
- Live telemetry printing (position, orientation, IMU, velocity).  
- Modular design using `robot_functions.bash`.

### 📦 Requirements
- ROS 2 Humble  
- `/robot_interface` parameters  
- `ros2 param` CLI  
- `bc` for float comparison

### 🎯 Focus
Reactive control, minimalist robotics tooling, and CLI‑driven robot behavior.

---

# 🐍 ROS 2 Obstacle Avoider in Python

**The Construct (July 2025)**  
Repository:  
https://github.com/Vanjoseluis/Academic_Projects/tree/main/Python_TurtleBot_Project

A ROS 2 node written in Python implementing reactive obstacle avoidance using LaserScan, IMU, odometry, and Twist commands.  
Designed for TurtleBot‑like robots.

### 🔧 Features
- Obstacle avoidance using frontal sectors (left, center, right).  
- Orientation tracking (yaw).  
- Reactive algorithm: turn or move forward based on distance readings.  
- Extensible architecture for navigation, mapping, or behavior trees.

### 📦 Requirements
- ROS 2 Humble  
- Python 3.10+  
- `rclpy`, `sensor_msgs`, `geometry_msgs`, `nav_msgs`

### 🎯 Focus
Python‑based ROS 2 node design, reactive navigation, and sensor‑driven control.

---

# 🔌 Digital Electronics Project — Combinational & Sequential System Design (VHDL, FPGA)

**University of Málaga — School of Industrial Engineering (May 2025)**  
Repository:  
https://github.com/Vanjoseluis/Academic_Projects/tree/main/Digital_Electronics

Two complementary digital systems designed using **VHDL**, **combinational logic**, and **finite state machines**, deployed on a **Nexys3 FPGA**.  
The project covers analytical derivation, Karnaugh minimization, schematic synthesis, simulation, and hardware validation.

### 🧩 Subsystems
- **Electronic Voting System** — combinational + sequential architecture for vote counting and evaluation.  
- **Secure Door Control FSM** — deterministic state machine with safety constraints and timeout logic.

### ⭐ Key Contributions
- Full combinational subsystem: vote counter, seven‑segment controller, majority evaluator.  
- Truth tables + Karnaugh maps for 256 combinations.  
- Sequential subsystem (Reg_Vot) as Moore FSM.  
- Supporting modules: ENA_GEN, Puls_On_Off, Ctrl_Leds.  
- Secure door FSM with 5 states (A–E), error handling, deterministic transitions.  
- Structured VHDL testbenches validating correct sequences and error recovery.  
- FPGA deployment with real‑time correctness under all scenarios.

### 📈 Impact
- Robust, modular digital systems combining combinational and sequential logic.  
- Strong capability in VHDL design, FSM synthesis, and hardware‑level debugging.  
- Full functional validation on FPGA hardware.  
- Professional documentation: state diagrams, transition tables, boolean functions, schematics, testbench structures, simulation analysis.

---

# 📌 Notes

Each academic project has its own dedicated page with:
- goals  
- architecture  
- roadmap  
- repository links  
- design notes  

More detailed write‑ups will be added over time.
