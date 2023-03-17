cmake_minimum_required(VERSION 3.0.0)

enable_language(ASM)

project(termux-bootstrap)

set(CMAKE_CXX_STANDARD 20)

add_library(${PROJECT_NAME} SHARED ${CMAKE_SOURCE_DIR}/src/termux-bootstrap.c ${CMAKE_SOURCE_DIR}/src/termux-bootstrap-zip.S)
set_target_properties(${PROJECT_NAME} PROPERTIES 
    LIBRARY_OUTPUT_DIRECTORY "${CMAKE_SOURCE_DIR}/lib/${ANDROID_ABI}"
)