cmake_minimum_required(VERSION 3.10)

project(MyProject
  VERSION 0.0.1
  DESCRIPTION "My Project"
  LANGUAGES CXX)

# set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++1y")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -O2")

link_directories(include)

enable_testing()

add_subdirectory(src)
add_subdirectory(tests)

