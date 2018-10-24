cmake_minimum_required(VERSION 2.8.3)
project(ardent_gazebo)

## Compile as C++11, supported in ROS Kinetic and newer
# add_compile_options(-std=c++11)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  gazebo_ros
  geometry_msgs
  sensor_msgs
  std_msgs
  gazebo
)


find_package(Boost REQUIRED COMPONENTS system thread)
find_package(gazebo REQUIRED)

include_directories(
  ${catkin_INCLUDE_DIRS}
  ${GAZEBO_INCLUDE_DIRS}
)
link_directories(${GAZEBO_LIBRARY_DIRS})

catkin_package(
  CATKIN_DEPENDS 
    sensor_msgs
    gazebo_ros 
  DEPENDS 
    gazebo
)

 #target_link_libraries(
# )
