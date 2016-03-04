cmake_minimum_required(VERSION 2.8)
project(poly2tri)
enable_language(CXX)

set(SOURCE_FILES poly2tri/common/shapes.cc
                 poly2tri/sweep/advancing_front.cc
                 poly2tri/sweep/cdt.cc
                 poly2tri/sweep/sweep.cc
                 poly2tri/sweep/sweep_context.cc)

include_directories(${CMAKE_SOURCE_DIR}/poly2tri)

add_library(poly2tri STATIC ${SOURCE_FILES})
