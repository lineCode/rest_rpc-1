cmake_minimum_required(VERSION 3.7)
project(test_client)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -pthread -std=c++11")

find_package(Boost COMPONENTS system REQUIRED)
include_directories(
        "../msgpack/include"
)

add_executable(test_client main.cpp)
target_link_libraries(test_client ${Boost_LIBRARIES})