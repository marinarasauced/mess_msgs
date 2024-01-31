cmake_minimum_required(VERSION 3.0.2)
project(messmsg)

find_package(catkin REQUIRED COMPONENTS
  message_generation
)

add_message_files(
  FILES
  MessToUAV.msg
  MessToUGV.msg
  MessToUGVLogger.msg
)

catkin_package(
  CATKIN_DEPENDS message_runtime
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)
