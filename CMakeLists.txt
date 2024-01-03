cmake_minimum_required(VERSION 3.12)

project(tiny-aes C)

add_library(${PROJECT_NAME} "")
target_sources(${PROJECT_NAME}
    PRIVATE
        ${CMAKE_CURRENT_LIST_DIR}/tinyaes.c
    INTERFACE
        ${CMAKE_CURRENT_LIST_DIR}/tinyaes.h
        ${CMAKE_CURRENT_LIST_DIR}/tinyaes.hpp
)

target_include_directories(${PROJECT_NAME}
    INTERFACE
        ${CMAKE_CURRENT_LIST_DIR}
)
