cmake_minimum_required(VERSION 3.28)
project(triangles)

set(CMAKE_CXX_STANDARD 26)

add_executable(triangles main.cpp)

find_package(glfw3 CONFIG REQUIRED)
target_link_libraries(triangles PRIVATE glfw)

find_package(glm CONFIG REQUIRED)
target_link_libraries(triangles PRIVATE glm::glm)

find_package(glad CONFIG REQUIRED)
target_link_libraries(triangles PRIVATE glad::glad)