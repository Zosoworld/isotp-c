cmake_minimum_required(VERSION 3.10)

# Project definition
project(isotp CXX)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++17 -Wno-psabi -Wall -Wextra -O3 -fno-exceptions")

# Get all include directories
include_directories(src)
# Compile isotp as Shared Lib
add_library(isotp SHARED src/isotp.cpp)

target_compile_options(isotp PUBLIC -fPIC)
target_include_directories(isotp PUBLIC src)