cmake_minimum_required(VERSION 3.10 FATAL_ERROR)

project(gravity_sim LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_VERBOSE_MAKEFILE ON)

find_package(glfw3 REQUIRED)
find_package(glm REQUIRED)
find_package(glew REQUIRED)
find_package(PkgConfig)
pkg_check_modules(gl REQUIRED gl)

add_executable(gravity_sim gravity_sim.cpp)
target_link_libraries(gravity_sim glfw GL glm glew)
add_executable(gravity_sim_3Dgrid gravity_sim_3Dgrid.cpp)
target_link_libraries(gravity_sim_3Dgrid glfw GL glm glew)
