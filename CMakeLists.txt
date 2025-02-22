cmake_minimum_required(VERSION 3.10)
project(cpp-lua)

# Set the C++ standard
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED True)

find_package(Lua REQUIRED)

message(STATUS "LUA_INCLUDE_DIR: ${LUA_INCLUDE_DIR}")

include_directories(/usr/local/include ${LUA_INCLUDE_DIR})

# Add executable
add_executable(cpp-lua
  cpp-lua.m.cpp
)

# Link lua library
target_link_libraries(cpp-lua
  lua
)