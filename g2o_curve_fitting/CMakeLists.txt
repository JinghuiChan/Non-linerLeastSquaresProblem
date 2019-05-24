cmake_minimum_required(VERSION 3.14)
project(g2o_curve_fitting)

set(CMAKE_CXX_STANDARD 14)

# 添加cmake模块以使用ceres库
list( APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/cmake_modules )

# 寻找G2O
find_package( G2O REQUIRED )
include_directories(
        ${G2O_INCLUDE_DIRS}
        "/usr/include/eigen3"
)

# OpenCV
find_package( OpenCV REQUIRED )
include_directories( ${OpenCV_DIRS} )

add_executable(g2o_curve_fitting main.cpp)

# 与G2O和OpenCV链接
target_link_libraries( g2o_curve_fitting
        ${OpenCV_LIBS}
        g2o_core g2o_stuff
        )