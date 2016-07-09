include_directories ("${PROJECT_SOURCE_DIR}/inc")

aux_source_directory(. SRCS)

include_directories(${Boost_INCLUDE_DIRS})

add_executable(client ${SRCS})
target_link_libraries(client ${Boost_LIBRARIES})

install(TARGETS client DESTINATION bin)
