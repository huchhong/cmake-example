cmake_minimum_required (VERSION 2.6)
project(echo)

# require boost
find_package(Boost REQUIRED COMPONENTS system)

set(CMAKE_CXX_FLAGS       "-Wall -std=c++11")

# osx need this
set(CMAKE_MACOSX_RPATH 1)

set(LIBRARY_OUTPUT_PATH ${PROJECT_BINARY_DIR}/lib)
set(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin)

# if this is set to on, then all libraries are built as shared libraries by default.
set(BUILD_SHARED_LIBS ON)

add_subdirectory (mylib)
add_subdirectory (server)
add_subdirectory (client)
