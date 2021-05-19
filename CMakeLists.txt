cmake_minimum_required(VERSION 3.16)

project(ROS_Cmake VERSION 1.0.0)


find_package(rclcpp REQUIRED)

find_package(std_msgs REQUIRED)

# include_directories(/opt/ros/foxy/include/rclcpp)
add_executable(ros2_cmake main.cpp)

target_link_libraries(ros2_cmake ${rclcpp_LIBRARIES})
target_include_directories(ros2_cmake PUBLIC ${rclcpp_INCLUDE_DIRS})
#include_directories(ros2_lib_cpp PRIVATE "/opt/ros/foxy/include/rclcpp")


message(STATUS "PATH = ${rclcpp_INCLUDE_DIRS}")
