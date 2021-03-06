# Gesture Detector with Openpose Software on ROS Kinetic

This repository aims to recognize gestures made by users. Recognized gestures can lead the robot to take certain actions and/or repeat user's movement.

## Table of Contents
* [Compatible Platforms](#compatible-platforms)
* [Hardware Requirements](#hardware-requirements)
* [Software Prerequisities](#software-prerequisities)
* [Installation](#installation)
* [License](#license)


## Compatible Platforms

This repository is written in standards-conforming Python. It is developed and tested on the following platforms:

1. Ubuntu 16.04
2. ROS Kinetic
3. Openpose Software
4. CUDA 8.0
5. OpenCV 3.2
6. Librealsense SDK 2.10.0+


## Hardware Requirements
Project uses following hardware:

1. Intel Core-i7 6700HQ
2. Nvidia Mobile Gtx 960
3. RealSense SR300 (Firmware 3.10.10.0 and up)
4. USB 3.0 Type-A port for camera connection


## Software Prequisities

As the ROS will be main environment it needs to be installed first. You may switch between camera and openpose installation. However completing step 3 before 4 is vital to prevent kernel errors.

1. Install ROS Kinetic. 
    
    http://wiki.ros.org/kinetic/Installation/Ubuntu

2. Install Openpose and OpenposeROS node following instructions below.

    https://github.com/firephinx/openpose_ros

Unless you want to use a separate camera skip step 3 and 4.

3. Install Realsense Camera Prerequisities.

    http://wiki.ros.org/librealsense#Installation_Prerequisites

4. Install Realsense Camera ROS Node from source.

    http://wiki.ros.org/realsense_camera/Tutorials/Building_librealsense_from_Sources

## Installation

1. Git clone the package into catkin workspace src folder.

    :~/path-to-catkin-workspace/catkin_ws/src$ git clone https://github.com/tolgasaglik/Gesture-Recognition-with-Openpose-ROS.git

Skip step 2 if you have already initialized your workspace.

2. Initialize your workspace.

    :~/catkin_ws$ catkin_init_workspace 

3. Build your package.

    :~/catkin_ws$ catkin_make

4. Source you environment.

    :~/catkin_ws$ source devel/setup.bash

5. Invoke the launcher. You may modify it if you want to use another camera.

    :~/catkin_ws$ roslaunch $(find gesture_detector)/launch/gesture_detector.launch

## License

Unless otherwise noted, gesture_detector repository is licensed under a BSD license (see LICENSE.bsd).

## Contributors

This is a non-exhaustive list of contributors:

* FranLera
