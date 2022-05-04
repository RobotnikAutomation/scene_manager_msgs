cmake_minimum_required(VERSION 3.0.2)
project(scene_manager_msgs)


set(MSG_DEPS
  std_msgs
  actionlib_msgs
  geometry_msgs
)

find_package(catkin REQUIRED COMPONENTS message_generation ${MSG_DEPS})

set(MSG_FILES
Layout.msg
)

set(SRV_FILES
ModifyObject.srv
SelectObjects.srv
MoveTo.srv
)

add_message_files(DIRECTORY msg FILES ${MSG_FILES})
add_service_files(DIRECTORY srv FILES ${SRV_FILES})

generate_messages(DEPENDENCIES ${MSG_DEPS})

catkin_package(CATKIN_DEPENDS message_runtime ${MSG_DEPS})




