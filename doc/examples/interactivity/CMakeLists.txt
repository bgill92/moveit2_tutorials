set(INTERACTIVITY_LIB_NAME interactivity_utils)

add_library(${INTERACTIVITY_LIB_NAME}
  src/interactive_robot.cpp
  src/imarker.cpp
  src/pose_string.cpp
)

target_include_directories(interactivity_utils 
  PRIVATE include)

#target_link_libraries(
#  ${INTERACTIVITY_LIB_NAME}
#  ${catkin_LIBRARIES}
#  ${Boost_LIBRARIES}
#)

ament_target_dependencies(interactivity_utils
  ${THIS_PACKAGE_INCLUDE_DEPENDS} Boost)

install(
  DIRECTORY include
  DESTINATION include/
)

install(
  TARGETS ${INTERACTIVITY_LIB_NAME}
  LIBRARY DESTINATION lib/${PROJECT_NAME}
  ARCHIVE DESTINATION lib/${PROJECT_NAME}
  RUNTIME DESTINATION lib/${PROJECT_NAME}
)

#install(DIRECTORY launch 
#  DESTINATION share/${PROJECT_NAME})
