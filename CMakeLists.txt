cmake_minimum_required(VERSION 3.10)

project(dummy
    LANGUAGES CXX
    VERSION 0.1.0
)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED True)
set(CMAKE_CXX_EXTENSIONS False)

set(CMAKE_EXPORT_COMMPILE_COMMANDS True)

add_executable(main main.cpp)
target_link_libraries(main
    PRIVATE
        cerberus-cpp
        yaml-cpp
)

add_subdirectory(external)
