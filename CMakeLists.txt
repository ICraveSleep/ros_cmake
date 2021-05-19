cmake_minimum_required(VERSION 3.16)

project(ROS_Cmake VERSION 1.0.0)


find_package(rclcpp REQUIRED)
#find_package(std_msgs REQUIRED)

add_executable(ros2_cmake main.cpp)

target_link_libraries(ros2_cmake ${rclcpp_LIBRARIES})
#target_include_directories(ros2_cmake PUBLIC ${rclcpp_INCLUDE_DIRS})


message(STATUS "rclcpp_INCLUDE_DIRS = ${rclcpp_INCLUDE_DIRS}")
#message(STATUS "libs = ${rclcpp_INCLUDE_DIRS}")
message(STATUS "rclcpp_LIBRARIES = /opt/ros/foxy/lib/*")
