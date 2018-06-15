cmake_minimum_required(VERSION 3.10)
project(HttpServer)
find_package(Boost 1.66)
set(CMAKE_CXX_STANDARD 11)
set(Boost_DEBUG ON)

set(LINK_DIR C:\\msys64\\mingw64\\lib)

link_directories("C:\\msys64\\mingw64\\lib")

include_directories("C:\\msys64\\mingw64\\include\\boost")

link_libraries(ws2_32 wsock32 boost_system-mt)

add_executable(HttpServer main.cpp server_base.h http_server.h handler.h)