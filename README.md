# 3DOF Robotic

A small 3-DOF robotic arm built from scratch in ROS 2 Jazzy as a learning project to understand the core ROS 2 concepts robot description, transforms, nodes, topics, visualization, and eventually kinematics.

## Current State

The arm is currently described using a custom URDF with:

- A cylindrical base
- Three links
- Three revolute joints
- A fixed end-effector
- Joint limits and visual materials

The URDF has been validated with `check_urdf` and is being visualized in RViz.

`robot_state_publisher` is publishing the robot's transforms, while `joint_state_publisher_gui` provides sliders for manually changing the three joint angles.

Current setup:

```text
URDF
 │
 ▼
robot_state_publisher
 │
 ├── /robot_description
 └── /tf
       ▲
       │
 /joint_states
       ▲
       │
joint_state_publisher_gui
       │
    sliders
       │
       ▼
      RViz
```
Some visuals:
<img width="1260" height="945" alt="image" src="https://github.com/user-attachments/assets/cebf9787-49e6-452f-a139-c2e10ad52236" />
