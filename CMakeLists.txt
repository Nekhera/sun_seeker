cmake_minimum_required(VERSION 3.0.2)
project(sun_seeker)

find_package(catkin REQUIRED COMPONENTS
  rospy
  rosgraph_msgs
  geometry_msgs
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES sun_seeker
#  CATKIN_DEPENDS rospy std_msgs
#  DEPENDS system_lib
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

catkin_install_python(PROGRAMS scripts/sun_seeker_node.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
