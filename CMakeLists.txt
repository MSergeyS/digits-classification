cmake_minimum_required(VERSION 3.8 FATAL_ERROR)
project(digits-classification)

set(CMAKE_CXX_STANDARD 17)
if(CMAKE_CXX_COMPILER_ID MATCHES "MSVC")
    set(
        CMAKE_CXX_FLAGS_DEBUG
        "${CMAKE_CXX_FLAGS_DEBUG} /JMC"
    )
else()
    set(
        CMAKE_CXX_FLAGS
        "${CMAKE_CXX_FLAGS} -Wall -Wextra -pedantic -Wno-unused-parameter -Wno-implicit-fallthrough"
    )
endif()

set(OpenCV_DIR "C:/dev/opencv/build")

find_package(OpenCV REQUIRED)

file(GLOB sources
    source/*.cpp
    source/*.h
)

add_executable( digits-classification ${sources})

target_link_libraries(digits-classification ${OpenCV_LIBS})

set_directory_properties(PROPERTIES VS_STARTUP_PROJECT digits-classification)
