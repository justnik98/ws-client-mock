cmake_minimum_required(VERSION 3.17)
project(asyncws)

set(CMAKE_CXX_STANDARD 20)

add_executable(asyncws main.cpp)

set(THREADS_PREFER_PTHREAD_FLAG ON)
find_package(Threads REQUIRED)
target_link_libraries(asyncws PRIVATE Threads::Threads)