cmake_minimum_required(VERSION 3.17)
project(timer)

set(CMAKE_CXX_STANDARD 20)

add_library(timer ${CMAKE_CURRENT_SOURCE_DIR}/src/timer.cpp)