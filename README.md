# Explorobot (ROS2)

## Introduction

Explorobot is a ROS2-based mobile robot simulation designed to explore unknown indoor environments, generate maps, and navigate autonomously.

The system focuses on building a complete robotics pipeline where the robot can perceive its surroundings, create a map in real time, and move within that environment without prior knowledge.

At this stage, the project is fully simulation-based using Gazebo and RViz, with plans to extend it to physical hardware in future iterations.

---

## Objective

The primary goal of Explorobot is to develop an end-to-end autonomous exploration system using ROS2, covering:

* Environment perception
* Real-time mapping
* Localization
* Autonomous navigation

---

## Core Capabilities

* Depth sensor-based environment perception
* Real-time map generation using SLAM
* Autonomous navigation using ROS2 Nav2 stack
* Robot modeling using URDF/Xacro
* Simulation in Gazebo with visualization in RViz

---

## Technologies Used

* ROS2
* Gazebo Simulator
* RViz2
* Nav2 (Navigation2)
* SLAM Toolbox
* URDF / Xacro

---

## System Workflow

The robot operates through the following pipeline:

Sensor Input → SLAM Processing → Map Creation → Localization → Path Planning → Movement Execution

This enables the robot to explore and navigate without relying on a pre-built map.

---

## Simulation Environment

* Custom Gazebo world for testing
* Depth camera used for perception
* Robot described using modular URDF/Xacro files
* RViz used for monitoring mapping and navigation

---

## Practical Applications

Explorobot represents systems used in real-world scenarios such as:

* Autonomous warehouse robots
* Indoor mapping and surveying
* Facility inspection and monitoring
* Service robots in structured environments
* Exploration of restricted or hazardous areas

---

## Strengths

* Demonstrates full autonomy pipeline in ROS2
* Modular design for easy upgrades
* Suitable base for real-world robotic systems
* Cost-effective approach using vision-based sensing

---

## Limitations

* Simulation-only (no hardware validation yet)
* Performance depends on simulated sensor accuracy
* Limited testing in complex dynamic environments
* No advanced obstacle prediction or AI-based planning

---

## Project Structure

```
explorobot/
├── config/
├── launch/
├── models/
├── rviz/
├── urdf/
├── worlds/
├── CMakeLists.txt
└── package.xml
```

---

## How to Run

### Build the workspace

```
cd ~/ros2_ws
colcon build
source install/setup.bash
```

### Launch the robot in simulation

```
ros2 launch explorobot explore_robot_gazebo.launch.xml
```

### Start mapping and navigation

```
ros2 launch explorobot nav2_slam.launch.py
```

---

## Challenges Encountered

* Stabilizing SLAM performance with simulated sensor input
* Managing coordinate transforms across different frames
* Configuring navigation parameters for smoother motion
* Ensing consistent behavior across different simulation runs

---

## Future Improvements

* Transition to real robot hardware
* Integrate physical depth camera
* Enhance navigation in dynamic environments
* Improve efficiency of mapping and planning
* Add intelligent decision-making capabilities

---

## Project Status

Explorobot is currently under active development and is not a finished system.

The current implementation focuses on achieving reliable simulation results. Future work will extend this into real-world deployment and more advanced capabilities.

---

## Final Thoughts

This project is aimed at understanding and implementing the complete lifecycle of an autonomous robot, from perception to action, using modern ROS2 tools.

---

## Project Status

This project is currently a work in progress and not a fully completed system.

The current focus is on building a stable simulation pipeline for autonomous exploration using ROS2. Hardware implementation and real-world testing are planned as the next phase.

Ongoing work includes improving navigation performance, handling more complex environments, and preparing the system for deployment on a physical robot.

---

## Author

Manjunadh
