cmake_minimum_required(VERSION 3.14)

project(glfw-boilerplate)

set(glfw_ROOT "P:/Downloads/cpp-libraries/glfw-3.3.6.bin.WIN64")
set(glad2_ROOT "P:/Downloads/cpp-libraries/glad2-web-generated")

SET(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} -static")

include_directories("${glad2_ROOT}/include" "${glfw_ROOT}/include")

add_executable(${PROJECT_NAME} WIN32
    "src/main.cpp"
)

target_link_libraries(${PROJECT_NAME} "${glfw_ROOT}/lib-mingw-w64/libglfw3.a")