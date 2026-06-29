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

This section summarizes the tools, academic work, and infrastructure I am building to improve reproducibility, introspection, and reliability in ROS 2 development.  
Each project reflects my focus on systems engineering, debugging, testing, and upstream contributions to the ROS 2 control ecosystem.

---

# 🎓 Academic Projects

A collection of university and training projects focused on robotics, automation, digital electronics, and applied systems engineering.

👉 Repository:  
https://github.com/Vanjoseluis/Academic_Projects

---

## 🏭 GEMMA Control System (TwinCAT 3)
Modular PLC architecture for the FMS 205 manufacturing station using TwinCAT 3, GEMMA methodology, SFC/GRAFCET, and real industrial hardware (sensors, cylinders, encoder, conveyor).  
Focus: deterministic task coordination, safe operation, and industry‑style control logic.

## 🐧 Bash Obstacle Avoider for ROS 2
Reactive obstacle avoidance implemented entirely in Bash using ROS 2 parameters, LaserScan, IMU, and odometry.  
Focus: minimalist robotics tooling, CLI‑based control loops, and real‑time decision logic.

## 🐍 Python Obstacle Avoider for ROS 2
ROS 2 node in Python implementing sector‑based obstacle avoidance with LaserScan, IMU, odometry, and Twist commands.  
Focus: clean architecture, extensible navigation logic, and sensor‑driven control.

## 🔌 Digital Electronics (VHDL, FPGA)
Two digital systems (Voting System + Secure Door FSM) designed with VHDL, combinational logic, Karnaugh minimization, Moore FSMs, and FPGA deployment.  
Focus: deterministic hardware behavior, timing analysis, and structured testbenches.

---

# 🧰 Personal Projects

Developer tooling and infrastructure aimed at improving reproducibility, debugging, and simulation reliability in ROS 2.

---

## 🔍 ros2-debug-assistant
Static analysis and automatic fixes for ROS 2 packages.  
Detects formatting issues, linter errors, missing dependencies, and CMake/manifest problems, with an interactive fix engine and modular architecture (CLI, analyzer, fixer, utils).  
Roadmap: ament_lint integration, dependency validation, launch/test diagnostics, VSCode extension.

## 🧪 autotest (planned)
Deterministic CI framework for `ros2_control` and `gz_ros2_control`.  
Provides multi‑run consistency checks, timing stability analysis, and automated regression detection for controllers and simulation pipelines.

## 🏎️ fastzebo (planned)
Exploration of a modern, ROS‑native fast simulation backend.  
Aims to improve startup determinism, reduce physics jitter, and optimize sensor/physics loops for high‑performance robotics simulation.

## 🕸️ ecosystem analyzer (TFG)
Graph‑based analysis of PR/Issue interactions in ros‑controls.  
Detects conflicting PRs, dependency chains, regressions, and cross‑distro divergence to support maintainers and reduce integration risk.

---

# 📌 Notes

Each project has its own dedicated page with:
- goals  
- architecture  
- roadmap  
- repository links  
- design notes  

More projects will be added as they evolve.

---

# 📝 Technical Notes

Short write‑ups on debugging, tests, controller_manager internals, and lessons learned while contributing to Open Source.

👉 [Notes](notes/)

---

# 📬 Contact

- GitHub: [@Vanjoseluis](https://github.com/Vanjoseluis)  
- LinkedIn: https://www.linkedin.com/in/josé-luis-pérez-martín
