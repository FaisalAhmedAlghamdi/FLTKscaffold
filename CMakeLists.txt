cmake_minimum_required(VERSION 3.10)
project("FLTscaffold")

# Add the FLTK submodule
set(FLTK_DIR ${CMAKE_SOURCE_DIR}/external/fltk)
add_subdirectory(${FLTK_DIR} fltk)

# Include directories
include_directories(${FLTK_DIR})

# Add your source files
add_executable(FLTscaffold WIN32 FLTscaffold.cpp)

# Link FLTK to your project
target_link_libraries(FLTscaffold fltk fltk_images fltk_forms fltk_gl)
