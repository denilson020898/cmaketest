cmake_minimum_required(VERSION 3.18.0)

project(cmaketest)

add_executable(${PROJECT_NAME} main.cpp)

add_subdirectory(adder)
target_link_directories(${PROJECT_NAME} PRIVATE adder)
target_include_directories(${PROJECT_NAME} PRIVATE adder)
target_link_libraries(${PROJECT_NAME} adder)