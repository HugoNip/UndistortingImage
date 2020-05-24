cmake_minimum_required(VERSION 3.0)
project(ch5)

set(CMAKE_CXX_STANDARD 11)

# OpenCV
find_package(OpenCV REQUIRED)
include_directories(${OpenCV_INCLUDES_DIRS})

# Executable
add_executable(undistortImage undistortImage.cpp)
target_link_libraries(undistortImage ${OpenCV_LIBS})
