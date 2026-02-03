cmake_minimum_required(VERSION 3.10)
project(dlsite_key_dumper VERSION 1.0.0)

# 使用 vcpkg 的 toolchain
if(DEFINED ENV{VCPKG_ROOT} AND NOT DEFINED CMAKE_TOOLCHAIN_FILE)
  set(CMAKE_TOOLCHAIN_FILE "$ENV{VCPKG_ROOT}/scripts/buildsystems/vcpkg.cmake"
      CACHE STRING "")
endif()

# 尋找 MinHook
find_package(minhook CONFIG REQUIRED)

add_subdirectory(src)