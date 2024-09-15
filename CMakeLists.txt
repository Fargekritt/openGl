cmake_minimum_required(VERSION 3.28)
project(openGl)

set(CMAKE_CXX_STANDARD 26)

add_executable(${PROJECT_NAME} src/main.cpp src/glad.c)

add_subdirectory(dependencies/glfw)

target_include_directories(${PROJECT_NAME} PUBLIC dependencies/glfw/include PUBLIC include)

target_link_directories(${PROJECT_NAME} PUBLIC dependencies/glfw/src)

target_link_libraries(${PROJECT_NAME} glfw)