cmake_minimum_required(VERSION 2.6)
project(pkg_capture)

add_executable(pkg_capture main.cpp)

install(TARGETS pkg_capture RUNTIME DESTINATION bin)
