cmake_minimum_required(VERSION 3.4.3)
project(ExternalProjectTest NONE)

include(ExternalProject)
ExternalProject_Add(A
                    PREFIX ${CMAKE_CURRENT_BINARY_DIR}/projects/A
                    SOURCE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/A
                    BINARY_DIR ${CMAKE_CURRENT_BINARY_DIR}/A
                    INSTALL_COMMAND ""
                    STEP_TARGETS configure build
                    BUILD_ALWAYS 1)
ExternalProject_Add(B
                    PREFIX ${CMAKE_CURRENT_BINARY_DIR}/projects/B
                    SOURCE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/B
                    BINARY_DIR ${CMAKE_CURRENT_BINARY_DIR}/B
                    INSTALL_COMMAND ""
                    STEP_TARGETS configure build
                    BUILD_ALWAYS 1)
