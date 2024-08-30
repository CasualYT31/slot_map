cmake_minimum_required(VERSION 3.14)

set_property(GLOBAL PROPERTY USE_FOLDERS ON)

set(PROJ_NAME SlotMap)
project(${PROJ_NAME})

set (CMAKE_CXX_STANDARD 17)

if(MSVC)
  add_definitions(-D_CRT_SECURE_NO_WARNINGS)
endif()

add_subdirectory("${PROJECT_SOURCE_DIR}/slot_map")
