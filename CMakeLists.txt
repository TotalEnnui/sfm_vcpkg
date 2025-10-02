cmake_minimum_required(VERSION 3.20)

project(sfml_vcpkg)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

set(SOURCE_FILES src/main.cpp)
set(PROJECT_TARGET main)

find_package(SFML CONFIG REQUIRED COMPONENTS 
        Graphics 
        Window 
        Audio 
        Network
)

add_executable(${PROJECT_TARGET} ${SOURCE_FILES})

target_link_libraries(${PROJECT_TARGET} PRIVATE
    SFML::Graphics
    SFML::Window
    SFML::Audio
    SFML::Network
)

install(TARGETS ${PROJECT_TARGET}
        RUNTIME DESTINATION bin
        LIBRARY DESTINATION lib
        ARCHIVE DESTINATION lib/static
)