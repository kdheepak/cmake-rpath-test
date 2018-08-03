cmake_minimum_required(VERSION 2.8.9)
project (hello)

set(CMAKE_MACOSX_RPATH 1)

include_directories(".")
file(GLOB SOURCES "./*.cpp")
add_library(shared_library SHARED ${SOURCES})


add_executable(hello main.cpp)

target_link_libraries(hello shared_library)

