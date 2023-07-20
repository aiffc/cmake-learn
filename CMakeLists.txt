cmake_minimum_required(VERSION 3.5 FATAL_ERROR)
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake")

set(DEMO demo)

project(${DEMO})

include_directories(${PROJECT_SOURCE_DIR}/inc)

file(GLOB COMPILE_FILES ${PROJECT_SOURCE_DIR}/src/**.c)

#add_definitions (-std=c11)
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -std=c11")

add_executable(${DEMO} ${COMPILE_FILES})