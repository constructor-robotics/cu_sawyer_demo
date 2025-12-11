cmake_minimum_required(VERSION 3.0.2)
project(cu_sawyer_demo)

find_package(catkin REQUIRED COMPONENTS
  moveit_commander
  rospy
  catkin_virtualenv
)

catkin_generate_virtualenv(
  INPUT_REQUIREMENTS requirements.in
)

catkin_package()

catkin_install_python(PROGRAMS
  scripts/face_detection
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

install(DIRECTORY data
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)