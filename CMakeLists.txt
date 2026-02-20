cmake_minimum_required(VERSION 3.5)
project(ros2_parameters)

# Find dependencies
find_package(ament_cmake REQUIRED)
find_package(rclcpp REQUIRED)

# Add executable
add_executable(param_node src/param_node.cpp)

# Link dependencies
ament_target_dependencies(param_node rclcpp)

# Install targets
install(TARGETS
  param_node
  DESTINATION lib/${PROJECT_NAME})

ament_package()
