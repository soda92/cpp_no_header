cmake_minimum_required(VERSION "3.16")
project(tlib)

find_package(fmt CONFIG REQUIRED)
add_library(print_hello print_hello.cpp print_hello.hpp)
target_link_libraries(print_hello PRIVATE fmt::fmt)

add_executable(hello hello.cpp)
target_link_libraries(hello PRIVATE print_hello)
