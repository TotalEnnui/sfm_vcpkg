cmake_minimum_required(VERSION 3.20)

project(sfml_vcpkg)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(SFML CONFIG REQUIRED COMPONENTS Graphics Window Audio Network)

message(STATUS "CMAKE_TOOLCHAIN_FILE = ${CMAKE_TOOLCHAIN_FILE}")

add_executable(main main.cpp)

target_link_libraries(main PRIVATE
    SFML::Graphics
    SFML::Window
    SFML::Audio
    SFML::Network
)
