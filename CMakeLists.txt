cmake_minimum_required(VERSION 3.22)

project(imgui_setup)


add_subdirectory("external")
find_package(OpenGL REQUIRED)
include_directories(${OPENGL_INCLUDE_DIRS})

find_package(glfw3 3.3 REQUIRED)
include_directories(${GLFW_INCLUDE_DIRS})
# ==== example =====

add_executable(${PROJECT_NAME} main.cpp)
# target_sources(${PROJECT_NAME} PUBLIC ${CMAKE_SOURCE_DIR})
target_link_libraries(${PROJECT_NAME} glfw ${GLFW_LIBRARIES} ${OPENGL_LIBRARIES})
target_link_libraries(${PROJECT_NAME} IMGUI)