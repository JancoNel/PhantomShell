# CMakeLists.txt
cmake_minimum_required(VERSION 3.5)
project(PHANTOMSHIELD)
add_executable(phantomshield main.cpp)


add_subdirectory(deps/sleepy-discord)
target_link_libraries(phantomshield sleepy-discord)