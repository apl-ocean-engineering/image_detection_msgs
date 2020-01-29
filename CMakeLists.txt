cmake_minimum_required(VERSION 2.8.3)
project(image_detection_msgs)


find_package(catkin REQUIRED COMPONENTS
  std_msgs
  sensor_msgs
  message_generation
)

add_message_files(
  FILES
  DetectionBox.msg
  DetectionBoxesList.msg
  SemanticDetectionMat.msg
  DetectionMetaData.msg
)

generate_messages(DEPENDENCIES std_msgs sensor_msgs)

catkin_package(CATKIN_DEPENDS message_runtime std_msgs sensor_msgs)
