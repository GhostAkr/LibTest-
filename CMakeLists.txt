cmake_minimum_required(VERSION 3.0.0)
project(LibTest++)

add_library(first SHARED src/first/first.h src/first/first.cpp)
add_library(second SHARED src/second/second.h src/second/second.cpp)

add_executable(main src/main.cpp)

# Switch order to use different definitions
# target_link_libraries(main first second)
target_link_libraries(main second first)
