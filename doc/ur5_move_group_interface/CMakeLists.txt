add_executable(ur5_move_group_interface src/ur5_move_group_interface.cpp)
target_link_libraries(ur5_move_group_interface ${catkin_LIBRARIES} ${Boost_LIBRARIES})
install(TARGETS ur5_move_group_interface DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})

