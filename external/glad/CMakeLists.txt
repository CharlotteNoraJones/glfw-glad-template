cmake_minimum_required(VERSION 3.15)

project(GLAD LANGUAGES C)

add_library(GLAD include/glad.h src/glad.c)

target_include_directories(GLAD PUBLIC include/)