cmake_minimum_required(VERSION 3.0)
project(linexa)

# add flags
#set(CMAKE_C_FLAGS "${CMAKE_CXX_FLAGS} -D_BSD_SOURCE -std=c11 -Wall -pedantic -Wextra")
set(CMAKE_C_FLAGS "${CMAKE_CXX_FLAGS} -D_BSD_SOURCE -std=c11 -pedantic -lm")

# get the PCA9685 lib
#find_library(PCA9685_LIBRARY PCA9685 HINTS /usr/local/lib)


# build
include_directories ("${PROJECT_SOURCE_DIR}/src")
add_executable (linexa src/linexa.c)
target_link_libraries(linexa ${PCA9685_LIBRARY})

# install
install(TARGETS linexa DESTINATION bin)
