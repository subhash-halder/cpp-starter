cmake_minimum_required(VERSION 3.17)

set(This Example)

project(${This} C CXX)

set(CMAKE_C_STANDARD 99)
set(CMAKE_CXX_STANDARD 11)

enable_testing()

# if (MSVC)
#   add_compile_options(/W4)
# else()
#   add_compile_options(-Wall -Wextra -Wpedantic)
# endif()

# add_subdirectory(googletest)

set(Headers
  Example.h
)

set(Sources
  Example.cpp
)

add_library(${This} STATIC ${Sources} ${Headers})

add_subdirectory(test)
