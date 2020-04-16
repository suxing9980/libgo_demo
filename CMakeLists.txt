cmake_minimum_required(VERSION 3.15)
project(libgo_demo)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_FLAGS "-std=c++17")


set(SOURCE_FILES main.cpp)

set(INC_DIR /build/libgo_lib/include)
set(LINK_DIR /build/libgo_lib/lib)

include_directories(${INC_DIR})
link_directories(${LINK_DIR})
link_libraries(libgo pthread dl)

add_executable(libgo_demo ${SOURCE_FILES})
#target_link_libraries(libgo_demo pthread dl)