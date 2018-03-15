cmake_minimum_required(VERSION 3.5)

project(test_dartsim_in_catkin)

find_package(catkin REQUIRED)

find_package(DART)


catkin_package(DEPENDS dartsim)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_EXTENSIONS OFF)

add_executable(someProgram src/main.cpp)
target_link_libraries(someProgram dart)
target_include_directories(someProgram DART_INCLUDE_DIRS)

