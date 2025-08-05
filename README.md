# controlling-robot-arm-by-joint_state

This project demonstrates how to visualize and control a robot arm in ROS2 using joint_state_publisher.

## Install Required Packages
sudo apt-get update && sudo apt-get install -y \
  ros-humble-joint-state-publisher-gui \
  ros-humble-gazebo-ros \
  ros-humble-xacro \
  ros-humble-ros2-control \
  ros-humble-ros2-controllers \
  ros-humble-joint-state-broadcaster \
  ros-humble-joint-trajectory-controller \
  ros-humble-controller-manager \
  ros-humble-moveit \
  ros-humble-gazebo-ros2-control

  ## Build the Workspace
  
  cd ~/ros2_ws
colcon build
source install/setup.bash

## Manual Fixes Applied

In order to make the robot arm appear and be controllable inside RViz2, the following changes were applied:

### 1. Fixed Frame

 • Changed from: map
 • To: world
 • This avoids the error:
Global Status: Frame 'map' does not exist

### 2. Robot Description

 • Added the RobotModel display in RViz:
 • Go to Add > select RobotModel
 • Ensure the correct topic is set
