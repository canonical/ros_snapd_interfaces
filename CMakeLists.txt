cmake_minimum_required(VERSION 3.16)
project(ros_snapd_interfaces)

find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)

rosidl_generate_interfaces(${PROJECT_NAME}
  "srv/SnapdList.srv"
  "srv/SnapdStart.srv"
  "srv/SnapdRestart.srv"
  "srv/SnapdStop.srv"
)

ament_export_dependencies(rosidl_default_runtime)
ament_package()
