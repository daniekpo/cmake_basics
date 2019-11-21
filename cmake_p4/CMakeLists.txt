cmake_minimum_required(VERSION 2.8)
project(Part4Project)

set(CMAKE_CXX_FLAGS "-Wall -std=c++0x")
if   (CMAKE_BUILD_TYPE STREQUAL Debug)
	set(BUILD_POSTFIX "_d")
else (CMAKE_BUILD_TYPE STREQUAL Debug)
	set(BUILD_POSTFIX "")
endif(CMAKE_BUILD_TYPE STREQUAL Debug)

include_directories(part4)
add_subdirectory(part4)
add_subdirectory(test)

add_executable(part3 main.cpp)
set_target_properties(part3 PROPERTIES RUNTIME_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR})
set_target_properties(part3 PROPERTIES DEBUG_POST_FIX "_d")

