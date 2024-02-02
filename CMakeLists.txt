cmake_minimum_required(VERSION 3.0.2)
project(mess_msgs)

find_package(catkin REQUIRED COMPONENTS
  std_msgs
  message_generation
)

add_message_files(
  FILES
  CalibrateUGV.msg
  MessToCV.msg
  MessToUAV.msg
  MessToUGV.msg
  MessToUGVLogger.msg
  StateUGV.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(
  CATKIN_DEPENDS std_msgs message_runtime
)
