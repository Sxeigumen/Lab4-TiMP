cmake_minimum_required(VERSION 3.16.3)
project(equation)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(equation equation.cpp)

include_directories(/mnt/c/Users/artem/workspace/Timp3/formatter_ex_lib)
include_directories(/mnt/c/Users/artem/workspace/Timp3/solver_lib)

target_link_libraries(equation formatter_ex)
target_link_libraries(equation solver)
