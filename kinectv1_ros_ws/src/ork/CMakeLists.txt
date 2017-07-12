cmake_minimum_required(VERSION 2.8.3)
project(ork)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS roscpp rospy std_msgs tf)
## System dependencies are found with CMake's conventions
# find_package(Boost REQUIRED COMPONENTS system)

catkin_package(
  INCLUDE_DIRS
#  LIBRARIES ork
#  CATKIN_DEPENDS other_catkin_pkg
#  DEPENDS system_lib
)

## Add folders to be run by python nosetests
# catkin_add_nosetests(test)
add_executable(ork_transform src/ork_transform.cpp)
target_link_libraries(ork_transform ${catkin_LIBRARIES})
add_executable(camera_base_tf_publish src/camera_base_tf_publish.cpp)
target_link_libraries(camera_base_tf_publish ${catkin_LIBRARIES})
