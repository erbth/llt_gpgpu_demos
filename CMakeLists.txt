cmake_minimum_required(VERSION 3.13)

project(llt_gpgpu_demos CXX)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=gnu++17 -O3 -Wall")
set(CMAKE_CXX_FLAGS_DEBUG "${CMAKE_CXX_FLAGS_DEBUG} -gdwarf-2")

# Find required packages
find_package(PkgConfig REQUIRED)
pkg_check_modules(XCB REQUIRED xcb xcb-dri2)
find_package(LltGpgpuRt REQUIRED)

add_subdirectory(src)
