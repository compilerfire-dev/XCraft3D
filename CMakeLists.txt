cmake_minimum_required(VERSION 3.10)
project(XCraft3D LANGUAGES CXX)

# Set C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Find packages
find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)
find_package(glm REQUIRED)
find_package(GLEW REQUIRED)

# Define the executable
add_executable(${PROJECT_NAME} src/main.cpp)

# Link libraries
target_link_libraries(${PROJECT_NAME} PRIVATE 
    OpenGL::GL
    glfw
    glm::glm
    GLEW::GLEW
    pthread 
    dl
)
