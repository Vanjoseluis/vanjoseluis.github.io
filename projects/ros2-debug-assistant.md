# ros2-debug-assistant

**Structural analysis tool for ROS 2**
It diagnoses common errors in ROS 2 packages and suggests automatic corrections.

## 🚀 Objective
Reduce friction in ROS 2 development by providing early, actionable diagnostics related to:
- Formatting and style 
- Missing or incorrect dependencies 
- CMake configuration
- Linters integration
- Introspection and structural analysis

## 🧱 Architecture
- CLI — entry point and user interface
- Analyzer — static analysis of files and package structure
- Fixer — automatic corrections and normalization
- Utils — shared helpers and utilities

## 🗺️ Roadmap

### v0.1.0 — MVP
- Basic formatting analysis
- Basic automatic fixes
- CLI with check/fix/interactive modes
- Unit tests for core functionality

### v0.2.0 — Linter integration
- Parse ament_lint output
- Provide explanations for common linter errors
- Suggest fixes

### v0.3.0 — Dependency & CMake analysis
- Detect missing dependencies
- Detect unused dependencies
- Validate CMakeLists.txt structure

### v0.4.0 — Test & launch diagnostics
- Detect common pytest/launch_testing issues
- Validate launch files

### v0.5.0 — Editor integration
- VSCode extension
- “Accept fix” UI
- Real-time diagnostics

Repository: 
[https://github.com/Vanjoseluis/ros2-debug-assistant](https://github.com/Vanjoseluis/ros2-debug-assistant)
