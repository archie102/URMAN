
cmake_minimum_required(VERSION 3.19)
project(URMAN)
set( GLFW_BUILD_DOCS OFF)

add_executable(${PROJECT_NAME} src/main.cpp)

add_subdirectory(external/glfw)

target_include_directories(${PROJECT_NAME}  
        PUBLIC 
            external/glfw/include)

target_link_directories(${PROJECT_NAME}  
        PRIVATE 
            external/glfw/src)
target_link_libraries(${PROJECT_NAME} PRIVATE glfw opengl32)
