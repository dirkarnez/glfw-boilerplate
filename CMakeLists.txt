cmake_minimum_required(VERSION 3.14)

project(glfw-boilerplate)

SET(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} -static")

include_directories("${GLAD2_ROOT}/include" "${GLFW_ROOT}/include")

add_executable(${PROJECT_NAME} WIN32
    "src/main.cpp"
)

target_link_libraries(${PROJECT_NAME} "${GLFW_ROOT}/lib-mingw-w64/libglfw3.a")