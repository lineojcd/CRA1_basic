cmake_minimum_required(VERSION 2.8.3)
project(augmented_reality_basics)

find_package(catkin REQUIRED COMPONENTS
  rospy
  duckietown_msgs
  image_geometry
)

catkin_package()
