cmake_minimum_required(VERSION 3.17)

project(ollvm-plug)

set(CMAKE_CXX_FLAGS "-Wall -fno-rtti")

find_package(LLVM REQUIRED CONFIG)

message(STATUS "Found LLVM ${LLVM_PACKAGE_VERSION}")
message("LLVM STATUS:
  Definitions ${LLVM_DEFINITIONS}
  Includes    ${LLVM_INCLUDE_DIRS}
  Libraries   ${LLVM_LIBRARY_DIRS}
  cmake file  ${LLVM_CMAKE_DIR}
  Targets     ${LLVM_TARGETS_TO_BUILD}"
        )

add_definitions(${LLVM_DEFINITIONS})
include_directories(${LLVM_INCLUDE_DIRS})
include_directories(ollvm/include)
add_subdirectory(ollvm)
