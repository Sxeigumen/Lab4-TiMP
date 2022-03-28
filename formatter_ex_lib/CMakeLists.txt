cmake_minimum_required(VERSION 3.16.3)
project(formatter_ex)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(formatter_ex STATIC formatter_ex.cpp formatter_ex.h)

include_directories(/mnt/c/Users/artem/workspace/Timp3/formatter_lib)
target_link_libraries(formatter_ex formatter)