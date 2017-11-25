cmake_minimum_required(VERSION 3.8)
project(cmake_link_library)

set(CMAKE_C_STANDARD 99)
add_library(CMAKE_EXERCISE STATIC IMPORTED)
set_target_properties(CMAKE_EXERCISE PROPERTIES IMPORTED_LOCATION "../libmylib.a")
set(SOURCE_FILES main.c)
add_executable(cmake_link_library ${SOURCE_FILES})
target_link_libraries(cmake_link_library CMAKE_EXERCISE)