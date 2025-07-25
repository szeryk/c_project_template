cmake_minimum_required(VERSION 3.10)

project(MyCProgram LANGUAGES C)

set(CMAKE_C_STANDARD 11)

add_executable(my_program main.c)

add_library(my_lib STATIC src/my_lib.c)
target_include_directories(my_lib PUBLIC include)

target_link_libraries(my_program PRIVATE my_lib)
