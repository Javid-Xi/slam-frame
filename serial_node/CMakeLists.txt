cmake_minimum_required(VERSION 2.8.3)
project( my_serial_node )

find_package(catkin REQUIRED COMPONENTS
  roscpp
  serial
  std_msgs
  tf
  nav_msgs
)

catkin_package(
  CATKIN_DEPENDS
    serial
    std_msgs
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

add_executable( serial_node src/serial_node.cpp)

target_link_libraries( serial_node
  ${catkin_LIBRARIES}
)

