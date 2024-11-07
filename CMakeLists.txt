cmake_minimum_required(VERSION 3.5.0)
project(CSockLib VERSION 0.1.0 LANGUAGES C)

file(GLOB_RECURSE SOURCES "src/**/*.c" "src/*.c")
file(GLOB_RECURSE HEADER_LIST "include/**/*.h" "include/*.h")

add_library(CSockLib ${SOURCES})

target_include_directories(CSockLib PUBLIC include)
target_link_directories(CSockLib PUBLIC src/**)

source_group(
      TREE "${CMAKE_CURRENT_LIST_DIR}/include"
        PREFIX "Header Files"
          FILES ${HEADER_LIST})