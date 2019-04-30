add_executable(pick_place_tutorial src/pick_place_tutorial.cpp)
target_link_libraries(pick_place_tutorial ${catkin_LIBRARIES} ${Boost_LIBRARIES})
install(TARGETS pick_place_tutorial DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})

add_executable(pick_place_tutorial_ur5 src/pick_place_tutorial_ur5.cpp)
target_link_libraries(pick_place_tutorial_ur5 ${catkin_LIBRARIES} ${Boost_LIBRARIES})
install(TARGETS pick_place_tutorial_ur5 DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})
