add_executable(visualizing_collisions_tutorial
  src/visualizing_collisions_tutorial.cpp
)

target_include_directories(visualizing_collisions_tutorial 
  PUBLIC include)

target_link_libraries(visualizing_collisions_tutorial
  interactivity_utils)

ament_target_dependencies(visualizing_collisions_tutorial
  ${THIS_PACKAGE_INCLUDE_DEPENDS} Boost)

install(TARGETS visualizing_collisions_tutorial 
  DESTINATION lib/${PROJECT_NAME})
  
install(DIRECTORY launch
  DESTINATION share/${PROJECT_NAME})
