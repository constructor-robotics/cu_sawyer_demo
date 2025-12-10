cmake_minimum_required(VERSION 3.0.2)
project(cu_sawyer_demo)

find_package(catkin REQUIRED COMPONENTS
  moveit_commander
  rospy
)

catkin_package()
