cmake_minimum_required(VERSION 3.0.0)

set(This GraphTest)

set(Sources
    GraphTest.cpp
)

add_executable(${This} ${Sources})

target_link_libraries(${This} PUBLIC
    gtest_main
    Graph
)
 
add_test(
    NAME ${This}
    COMMAND ${This}
)