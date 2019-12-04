cmake_minimum_required(VERSION 3.12)
project(RPI_project)

set(this RPIproject)
set(CMAKE_CXX_STANDARD 11)

set(CMAKE_POSITION_INDEPENDENT_CODE ON)
enable_testing()
add_subdirectory(googletest)
add_subdirectory(opencv)


#include_directories(PIproject)

set (Headers
        PIproject/shared.h
	)

set(Sources
        PIproject/main.cpp
	)

add_library(${this} STATIC ${Sources} ${Headers})

add_subdirectory(tests)





