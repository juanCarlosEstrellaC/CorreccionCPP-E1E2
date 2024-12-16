cmake_minimum_required(VERSION 3.29)
project(correccionEjercicio2)

set(CMAKE_CXX_STANDARD 17)

# MPI
find_package(MPI)
if (MPI_FOUND)
    message(STATUS "MPI FOUD")
    message(STATUS "MPI Include path: ${MPI_CXX_VERSION}")
    message(STATUS "MPI Include path: ${MPI_INCLUDE_PATH}")
    message(STATUS "MPI Libraries: ${MPI_LIBRARIES}")
    message(STATUS "MPI Include path: ${MPI_CXX_COMPILER}")
    message(STATUS "MPI Include path: ${MPI_lINK_FLAGS}")
else ()
    message(FATAL_ERROR "MPI Not FOUND")
endif ()
include_directories(${MPI_INCLUDE_PATH})

add_executable(correccionEjercicio2 main.cpp)

target_link_libraries(correccionEjercicio2 ${MPI_LIBRARIES})


