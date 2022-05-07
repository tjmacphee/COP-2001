cmake_minimum_required(VERSION 3.21)

set(CMAKE_OSX_ARCHITECTURES x86_64)

project(Breakout1)

add_executable(Breakout1 breakout1.cpp breakout_defs.h)

set(CMAKE_CXX_STANDARD 17)

set(SFML_INCLUDE_DIR "/usr/local/include")
set(SFML_LIBRARY_DIR "/usr/local/lib")

find_package(SFML 2.5.1 COMPONENTS system window graphics network audio)

target_link_libraries(Breakout1 sfml-graphics sfml-window sfml-system)