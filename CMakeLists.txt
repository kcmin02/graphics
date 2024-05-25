cmake_minimum_required(VERSION 3.28)
project(mygraphics)

set(CMAKE_CXX_STANDARD 17)
include_directories( SYSTEM "gladfile/include" )

add_executable(mygraphics main.cpp
        gladfile/src/glad.c)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)

add_subdirectory(glfw-3.4)

target_link_libraries(mygraphics glfw)



