
# Requirement: Set `VCPKG_ROOT` to the folder that contains vcpkg source

cmake_minimum_required(VERSION 3.16 FATAL_ERROR)

set(ENV{VCPKG_FEATURE_FLAGS} "manifests,registries,versions")
set(VCPKG_INSTALL_OPTIONS "--debug")
if(NOT DEFINED CMAKE_TOOLCHAIN_FILE) # Can't use `coveo_set_if_not_defined` because of `CACHE STRING ""`
    set(CMAKE_TOOLCHAIN_FILE "$ENV{VCPKG_ROOT}/scripts/buildsystems/vcpkg.cmake" CACHE STRING "")
endif()

project(toyprojectvcpkg LANGUAGES CXX VERSION 8.2.0.0) # See coveo_set_product_versions_if_not_overriden

add_executable(toyprojectvcpkg_main ${CMAKE_CURRENT_LIST_DIR}/main.cpp)
