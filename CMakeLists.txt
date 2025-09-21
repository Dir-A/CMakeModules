cmake_minimum_required(VERSION 3.25)

# Project
project("zqf_cmake_modules" VERSION 1.0)

# Library
add_library(${PROJECT_NAME} INTERFACE)

# Install
include("cmake/ZQF_Installer.cmake")
zqf_installer(${PROJECT_NAME} CONFIG_TEMPLATE_PATH "${CMAKE_SOURCE_DIR}/Config.cmake.in")
install(DIRECTORY "${CMAKE_SOURCE_DIR}/cmake" DESTINATION "share/cmake/${PROJECT_NAME}")