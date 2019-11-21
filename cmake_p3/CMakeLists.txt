cmake_minimum_required(VERSION 2.8)
project(Part3Project)


set(STRING_VARIABLE "value")
set(LIST_VARIABLE "value1 value2")

message("The value of STRING_VARIABLE is ${STRING_VARIABLE}")

set(CMAKE_CXX_FLAGS "-Wall -std=c++0x")
message("CMAKE_BUILD_TYPE is ${CMAKE_BUILD_TYPE}")

add_executable(part3 main.cpp)
set_target_properties(part3 PROPERTIES RUNTIME_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR})
set_target_properties(part3 PROPERTIES DEBUG_POST_FIX "_d")

