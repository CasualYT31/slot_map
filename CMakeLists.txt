cmake_minimum_required(VERSION 3.14)

set_property(GLOBAL PROPERTY USE_FOLDERS ON)

set(PROJ_NAME SlotMapTest)
project(${PROJ_NAME})

set (CMAKE_CXX_STANDARD 17)

if(MSVC)
  target_compile_options(${PROJ_NAME} PRIVATE /W4 /WX)
  add_definitions(-D_CRT_SECURE_NO_WARNINGS)
else()
  target_compile_options(${PROJ_NAME} PRIVATE -Wall -Wextra -pedantic -Werror)
endif()

# add slot_map
add_subdirectory("${PROJECT_SOURCE_DIR}/slot_map")
target_link_libraries(${PROJ_NAME} slot_map)
