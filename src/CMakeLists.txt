cmake_minimum_required(VERSION 3.8)
project(MPAGSCipher VERSION 0.1.0)

set(CMAKE_VERBOSE_MAKEFILE ON)


# specifics of our build
set(CMAKE_CXX_EXTENSIONS off)
set(CMAKE_CXX_FLAGS "-Wall -Wextra -Werror -Wfatal-errors -Wshadow -pedantic")

# Declare the build
add_executable(mpags-cipher mpags-cipher.cpp
  MPAGSCipher/TransformChar.hpp
  MPAGSCipher/TransformChar.cpp
)
target_include_directories(mpags-cipher PRIVATE MPAGSCipher)
target_compile_features(mpags-cipher PRIVATE cxx_std_17)