cmake_minimum_required(VERSION 3.10)

file(GLOB CONTENT_SOURCE "*.cpp")
add_library(iodate ${CONTENT_SOURCE})

target_include_directories(iodate PUBLIC ${CMAKE_ROOT}/include/iodate)

