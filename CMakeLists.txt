cmake_minimum_required(VERSION 3.10)

set(CMAKE_CXX_STANDARD 14)

project(DankaProject)

set(SOURCE_EXE src/main.cpp)

set(SOURCE_LIB src/name.cpp)

set(SOURCE_HEADER src/name.h)

add_library(
    name STATIC 
    ${SOURCE_LIB} 
    ${SOURCE_HEADER}
    )

target_include_directories(
    name
    PUBLIC
    "src"
)

add_executable(main ${SOURCE_EXE})

target_link_libraries(main name)
