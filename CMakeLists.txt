cmake_minimum_required(VERSION 3.25)

project(ping
    VERSION 0.0.1
    DESCRIPTION "This is my Project"
    LANGUAGES CXX)
message(STATUS "👉PROJECT_BINARY_DIR = ${PROJECT_BINARY_DIR}")
message(STATUS "👉PROJECT_SOURCE_DIR = ${PROJECT_SOURCE_DIR}")

set(PROJECT ping4)

set(CMAKE_C_STANDARD 17)
set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

file(GLOB_RECURSE SRC_FILES Src/*.cpp)

add_executable(${PROJECT} ${SRC_FILES})

target_compile_features(${PROJECT} PRIVATE cxx_std_23)

target_include_directories(${PROJECT} PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/Inc)