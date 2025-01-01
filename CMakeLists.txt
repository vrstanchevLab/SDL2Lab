cmake_minimum_required(VERSION 3.10)

project(SDL2AndroidApp)

# Add the source file
add_library(main SHARED main.c)

# Set the SDL2 library path (update this if needed)
set(SDL2_DIR ${CMAKE_SOURCE_DIR}/libs/SDL2)

# Include SDL2 headers
include_directories(${SDL2_DIR}/include)

# Link the SDL2 library
add_subdirectory(${SDL2_DIR} ${CMAKE_BINARY_DIR}/sdl2)
target_link_libraries(main SDL2)
