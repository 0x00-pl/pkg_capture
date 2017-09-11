cmake_minimum_required(VERSION 2.6)
project(pkg_capture)

SET(CMAKE_C_FLAGS "-Wall -Wextra")

#set(CMAKE_C_COMPILER "scan-build ${CMAKE_C_COMPILER}")
#set(CMAKE_CXX_COMPILER "scan-build ${CMAKE_CXX_COMPILER}"
#set($env(CC) "scan-build ${CC}")
#set($env(CXX) "scan-build ${CXX}")

add_executable(pkg_capture sniffex.cpp)
target_link_libraries(pkg_capture pcap)

install(TARGETS pkg_capture RUNTIME DESTINATION bin)
