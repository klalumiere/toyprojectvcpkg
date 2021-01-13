
# Requirement: Set `VCPKG_ROOT` to the folder that contains vcpkg source

cmake_minimum_required(VERSION 3.16 FATAL_ERROR)

set(ENV{VCPKG_FEATURE_FLAGS} "manifests,registries,versions")
set(VCPKG_INSTALL_OPTIONS "--debug")
if(NOT DEFINED CMAKE_TOOLCHAIN_FILE)
    set(CMAKE_TOOLCHAIN_FILE "$ENV{VCPKG_ROOT}/scripts/buildsystems/vcpkg.cmake" CACHE STRING "")
endif()

project(toyprojectvcpkg LANGUAGES CXX)

add_executable(toyprojectvcpkg_main ${CMAKE_CURRENT_LIST_DIR}/main.cpp)
