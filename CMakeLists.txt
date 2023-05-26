# Minimum version of CMake required to build the project
cmake_minimum_required(VERSION 3.10)

# Project name
project(detest)

# Set the C++ standard to C++17
set(CMAKE_CXX_STANDARD 17)

# Set the C standard to C11
set(CMAKE_C_STANDARD 11)

# Add the source files to the project
set(SOURCES
    src/de.h
        src/epsplot.h
    src/polyeval.h
    src/detest.cpp
)

# Create the executable target
add_executable(${PROJECT_NAME} ${SOURCES})

# Set any additional compiler flags
target_compile_options(${PROJECT_NAME} PRIVATE -Wall -Wextra)
