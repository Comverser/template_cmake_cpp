cmake_minimum_required (VERSION 3.5)

project(template_cmake_cpp)

set(CMAKE_BUILD_TYPE Debug)
#set(CMAKE_BUILD_TYPE Release)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++14")

include_directories(${PROJECT_SOURCE_DIR}/src/apps)
include_directories(${PROJECT_SOURCE_DIR}/src/libs)

file(GLOB SOURCES_APPS "src/apps/*.cpp")
file(GLOB SOURCES_LIBS "src/libs/*.cpp")

add_executable(demo ${SOURCES_APPS} ${SOURCES_LIBS})
