# set minimum cmake version
cmake_minimum_required(VERSION 3.5 FATAL_ERROR)

# project name and language
project(ffan_op LANGUAGES C)

message(STATUS "CMAKE_CURRENT_SOURCE_DIR ${CMAKE_CURRENT_SOURCE_DIR}")

add_subdirectory(src)
add_subdirectory(test)

add_executable(hello-world hello-world.c)

install(
    TARGETS myop test_op hello-world
    LIBRARY DESTINATION ${CMAKE_CURRENT_BINARY_DIR}/lib
    ARCHIVE DESTINATION ${CMAKE_CURRENT_BINARY_DIR}/lib
    RUNTIME DESTINATION ${CMAKE_CURRENT_BINARY_DIR}/bin
    PUBLIC_HEADER DESTINATION include
)