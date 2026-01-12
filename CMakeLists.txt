cmake_minimum_required(VERSION 3.10)
project(learn-opengl)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# 1. find packages (added by vcpkg)
find_package(glfw3 CONFIG REQUIRED)
find_package(glm CONFIG REQUIRED)
find_package(glad CONFIG REQUIRED)

# 2. make executable
add_executable(App src/main.cpp)

# 3. Link
target_link_libraries(App PRIVATE glfw glad::glad glm::glm)