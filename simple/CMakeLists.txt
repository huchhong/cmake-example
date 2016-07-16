cmake_minimum_required (VERSION 2.6)
project(test)

set(CMAKE_CXX_FLAGS       "-Wall -std=c99")

set(LIBRARY_OUTPUT_PATH ${PROJECT_BINARY_DIR}/lib)
set(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin)

aux_source_directory (. SRCS)
add_executable (server ${SRCS})
#target_link_libraries(server ${Boost_LIBRARIES} ev)
install(TARGETS server DESTINATION bin)
