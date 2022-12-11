cmake_minimum_required(VERSION 3.8)
project(cmake_example CXX)

add_library(mylib
    src/mylibfile.hpp
    src/mylibfile.cpp)

add_executable(server src/server.cpp)

add_executable(client src/client.cpp)

target_link_libraries(example mylib)

target_include_directories(client src)
target_include_directories(server src)
set_target_properties(client server mylib CXX_STANDARD 17)
