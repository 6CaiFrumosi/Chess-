cmake_minimum_required(VERSION 3.10 FATAL_ERROR)
project(chess++)

add_executable(${PROJECT_NAME} main.cpp)

add_subdirectory(SDL2-2.30.8)

target_include_directories(${PROJECT_NAME} PRIVATE SDL2-2.30.8/include)
link_directories(${CMAKE_SOURCE_DIR}/builddir)
target_link_libraries(${PROJECT_NAME} PRIVATE SDL2)