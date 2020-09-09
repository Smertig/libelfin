cmake_minimum_required(VERSION 3.1)
project(libelfin)

set(CMAKE_CXX_STANDARD 11)

add_subdirectory(elf)
add_subdirectory(dwarf)
add_subdirectory(examples)

add_library(libelfin ALIAS libelfin-dwarf)
