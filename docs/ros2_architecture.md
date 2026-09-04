# ROS 2 Architecture

## What I have built

The current system consists of my URDF, robot_state_publisher,
joint_state_publisher_gui and RViz.

The URDF describes the physical/kinematic structure of the arm:

base_link
    |
  joint1
    |
  link1
    |
  joint2
    |
  link2
    |
  joint3
    |
  link3
    |
end_effector

## Runtime architecture

URDF
  |
  v
robot_state_publisher
  |
  +---- /tf
  |
  +---- /robot_description
  |
  ^
  |
/joint_states
  ^
  |
joint_state_publisher_gui
  |
  v
joint sliders

RViz subscribes to the relevant information and renders the robot.

## What I understand


## Things I still don't understand

