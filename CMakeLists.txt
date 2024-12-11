cmake_minimum_required(VERSION 3.21)

project(gd-render-texture)

add_library(gd-render-texture INTERFACE)

set_target_properties(gd-render-texture PROPERTIES CXX_VISIBILITY_PRESET hidden)

target_sources(gd-render-texture INTERFACE
    ${CMAKE_CURRENT_SOURCE_DIR}/RenderTexture.cpp
)

target_include_directories(gd-render-texture INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)
