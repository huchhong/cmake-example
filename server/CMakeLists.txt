include_directories ("${PROJECT_SOURCE_DIR}/inc")

aux_source_directory (. SRCS)

include_directories(${Boost_INCLUDE_DIRS})
include_directories("${PROJECT_SOURCE_DIR}/mylib")

add_executable (server ${SRCS})
target_link_libraries(server ${Boost_LIBRARIES} mylib)

install(TARGETS server DESTINATION bin)
