cmake_minimum_required(VERSION 3.14)
project(Gauss_Newton)

set(CMAKE_CXX_STANDARD 14)

FIND_PACKAGE(OpenCV REQUIRED)

INCLUDE_DIRECTORIES("/usr/include/eigen3/"
        ${OpenCV_INCLUDE_DIRS})

add_executable(Gauss_Newton main.cpp)

TARGET_LINK_LIBRARIES(${PROJECT_NAME}
        ${OpenCV_LIBS})