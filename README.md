# ROS REALITY BRIDGE

Hi, and welcome to ROS Reality Bridge, a virtual reality teleoperation interface for ROS enabled robots. This readme contains all the information you need to get started.

## Notes about this fork

We use this package for the PR2 so we've removed extra files and dependencies that aren't needed for that purpose.

## Overview

This package connects a ROS network to a remote windows machine running Unity, and uses sensor data sent on ROS topics to populate a virtual reality scene. The sensors we use are a Kinect v2, the wrist cameras of the robot, and the joint encoders of the robot.

## Installation

You will need to install rosbridge via apt-get ```sudo apt-get install ros-<rosdistro>-rosbridge-suite```

Then clone this package into the src folder of your catkin workspace and build your workspace.

## Extras

To connect the Kinect to the ROS network, we use IAI Kinect, a ROS package found here: https://github.com/code-iai/iai_kinect2

To calibrate the Kinect, we use this package: https://github.com/ShibataLabPrivate/kinect_baxter_calibration

## Running ROS Reality

To start ROS Reality, simply run the following command in your catkin workspace:

``roslaunch ros_reality_bridge ros_reality_bridge.launch``

To ensure this package is working correctly, check if messages are being published to `/ros_unity` (```rostopic echo /ros_unity```).
