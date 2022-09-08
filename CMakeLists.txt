cmake_minimum_required(VERSION 3.10)

project("ringbuffer" LANGUAGES C)

add_library(ringbuffer OBJECT ringbuffer.c ringbuffer.h)

set_target_properties(ringbuffer
    PROPERTIES
    C_STANDARD 99
)

target_include_directories(ringbuffer
    PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
)