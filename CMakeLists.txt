cmake_minimum_required(VERSION 3.20)
project(razermacos C CXX)

file(GLOB_RECURSE SOURCES RELATIVE ${CMAKE_SOURCE_DIR} "src/main/*.c" "src/main/*.cc")
add_library(razermacos SHARED ${SOURCES})
target_include_directories(razermacos PUBLIC "src/include")
target_link_libraries(razermacos "-framework IOKit")
target_link_libraries(razermacos "-framework CoreFoundation")