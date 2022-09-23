# CMakeLists.txt file for larfinder

#  This simply copies files into an install directory - there is no build

cmake_minimum_required(VERSION 3.20 FATAL_ERROR)

find_package(cetmodules REQUIRED)
project(larfinder VERSION 09.00.00 LANGUAGES NONE)

include(CetCMakeEnv)

# larfinder has no architecture dependence
cet_cmake_env()

cet_cmake_module_directories(Modules BINARY)

# source
add_subdirectory(Modules)

cet_cmake_config(ARCH_INDEPENDENT)


