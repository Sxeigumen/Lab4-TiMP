cmake_minimum_required(VERSION 3.16.3)
project(hello_world)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(hello_world hello_world.cpp)

include_directories(/mnt/c/Users/artem/workspace/Timp3/formatter_ex_lib)
target_link_libraries(hello_world formatter_ex)