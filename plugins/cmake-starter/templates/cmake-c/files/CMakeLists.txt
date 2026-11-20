cmake_minimum_required(VERSION 3.16)
project(app C)

set(CMAKE_C_STANDARD 11)
add_compile_options(-Wall -Wextra)

add_executable(app src/main.c)
