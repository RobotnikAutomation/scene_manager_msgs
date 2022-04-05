cmake_minimum_required(VERSION 3.0.2)
project(scene_manager_msgs)


set(MSG_DEPS
  std_msgs
  actionlib_msgs
)

find_package(catkin REQUIRED COMPONENTS message_generation ${MSG_DEPS})


set(SRV_FILES
ModifyObjects.srv
)

add_service_files(DIRECTORY srv FILES ${SRV_FILES})

generate_messages(DEPENDENCIES ${MSG_DEPS})

catkin_package(CATKIN_DEPENDS message_runtime ${MSG_DEPS})




