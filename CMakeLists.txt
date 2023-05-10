cmake_minimum_required(VERSION 3.22)

project(imgui_setup)


set(CMAKE_CXX_STANDARD 17)

# Add GLFW library
find_package(glfw3 3.3 REQUIRED)
include_directories(${GLFW_INCLUDE_DIRS})

# Add ImGui library
set(IMGUI_DIR "${CMAKE_CURRENT_SOURCE_DIR}/external/imgui")
include_directories(${IMGUI_DIR})



# Add your project executable
add_executable(imgui_setup main.cpp)

# Link GLFW and ImGui libraries to your project executable
target_link_libraries(imgui_setup glfw ${GLFW_LIBRARIES} ${IMGUI_DIR}/imgui.cpp)