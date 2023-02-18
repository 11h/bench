cmake_minimum_required(VERSION 3.24)
project(bench)

set(CMAKE_CXX_STANDARD 17)

include(FetchContent)

FetchContent_DECLARE(
        nanobench
        GIT_REPOSITORY https://github.com/martinus/nanobench.git
        GIT_TAG v4.1.0
        GIT_SHALLOW TRUE
)
FetchContent_MakeAvailable(nanobench)

add_executable(bench main.cpp)

target_link_libraries(bench PRIVATE nanobench)
