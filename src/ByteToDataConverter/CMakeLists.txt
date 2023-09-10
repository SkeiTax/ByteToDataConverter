cmake_minimum_required(VERSION 3.10)

file(GLOB CONTENT_SOURCE "*.cpp")
add_library(btdconv ${CONTENT_SOURCE})

target_include_directories(btdconv PUBLIC ${CMAKE_ROOT}/include/btdconv)

