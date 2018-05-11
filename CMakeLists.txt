cmake_minimum_required(VERSION 2.8)
INCLUDE(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
CONAN_BASIC_SETUP()
project(json11)

add_library(json11 json11.cpp)
target_include_directories(json11 PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
target_compile_options(json11
  PRIVATE -fPIC -fno-rtti -fno-exceptions -Wall)
