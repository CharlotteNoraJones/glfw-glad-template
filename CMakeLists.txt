cmake_minimum_required(VERSION 3.15)

include(FetchContent)

FetchContent_Declare(
    glfw
    GIT_REPOSITORY https://github.com/glfw/glfw
    GIT_TAG 3.4
    GIT_PROGRESS TRUE
)
FetchContent_MakeAvailable(glfw)

add_subdirectory(external/glad/)

project(OpenGLTemplate LANGUAGES C CXX)

add_executable(OpenGLTemplate src/main.cpp)

target_link_libraries(OpenGLTemplate PRIVATE GLAD)
target_link_libraries(OpenGLTemplate PRIVATE glfw)