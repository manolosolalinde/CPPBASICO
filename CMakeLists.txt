cmake_minimum_required(VERSION 3.5)
project( DisplayImage )
find_package( OpenCV REQUIRED )
include_directories( ${OpenCV_INCLUDE_DIRS} )

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Werror -g") #include -g for debug information
set(source_dir "${PROJECT_SOURCE_DIR}/src/")
file (GLOB source_files "${source_dir}/*.cpp")

set(CMAKE_VERBOSE_MAKEFILE ON) #comment to use `make VERBOSE=1`


add_executable(DisplayImage ${source_files})
target_link_libraries( DisplayImage ${OpenCV_LIBS} )

