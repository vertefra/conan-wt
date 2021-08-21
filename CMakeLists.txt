cmake_minimum_required(VERSION 3.13)  # CMake version check
project(simple_example)               # Create project "simple_example"

add_definitions("-std=c++14")
include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

add_executable(main_exe main.cpp)

target_link_libraries(main_exe ${CONAN_LIBS})

