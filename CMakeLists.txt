cmake_minimum_required(VERSION 3.0.0)
project(Graph VERSION 0.1.0)

enable_testing()

set(CMAKE_ENABLE_EXPORTS ON)
set(CMAKE_POSITION_INDEPENDENT_CODE ON)

add_executable(Graph Graph.cpp)
add_subdirectory(googletest)
add_subdirectory(test)

set(Headers
    Graph.hpp
)
set(Sources
    Graph.cpp

)

add_library(${Graph} STATIC ${Sources} ${Headers})
