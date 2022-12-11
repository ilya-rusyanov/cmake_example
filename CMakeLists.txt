cmake_minimum_required(VERSION 3.8)
project(cmake_example CXX)

add_library(mylib src/mylibfile.cpp)

add_executable(example src/main.cpp)

target_link_libraries(example mylib)
