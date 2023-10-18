cmake_minimum_required(VERSION 3.5)
project(action_msg_srv)

include(cmake/declarations.cmake)
include(cmake/dependecies.cmake)

rosidl_generate_interfaces(${PROJECT_NAME}
  "srv/Translation.srv"
  "srv/Rotation.srv"
  "srv/StateSwitch.srv"
  "srv/MotorPosition.srv"
  "srv/MotorSpeed.srv"
  "srv/TranslationAcceleration.srv"
  "srv/TranslationSpeed.srv"
  "srv/RotationAcceleration.srv"
  "srv/RotationSpeed.srv"
  "msg/MotionStatus.msg"
  "msg/MotionSpeed.msg"
)

if(BUILD_TESTING)
  find_package(ament_lint_auto REQUIRED)
  ament_lint_auto_find_test_dependencies()
endif()

ament_package()