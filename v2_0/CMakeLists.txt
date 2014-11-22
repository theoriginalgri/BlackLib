cmake_minimum_required (VERSION 2.6)

project (BlackLib)

# add all the cpp files to the library 
file(GLOB SOURCES ./*.cpp)

list(APPEND CMAKE_CXX_FLAGS "-std=c++11 ${CMAKE_CXX_FLAGS} -g -ftest-coverage -fprofile-arcs")

add_library (BlackLib ${SOURCES})

target_include_directories (BlackLib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

# add the example
add_subdirectory(exampleAndTiming)
