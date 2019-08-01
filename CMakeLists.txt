cmake_minimum_required(VERSION 2.8.3)
project(ros_reality_bridge)

find_package(catkin REQUIRED COMPONENTS
  rospy
  std_msgs
  sensor_msgs
)


include_directories(
  ${catkin_INCLUDE_DIRS}
)

