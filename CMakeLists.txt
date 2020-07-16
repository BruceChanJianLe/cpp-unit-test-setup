cmake_minimum_required(VERSION 3.8)

# Set variable "This" with "Example"
set(This Checkout)

project(${This} CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_POSITION_INDEPENDENT_CODE ON)

# Enable unit testing
enable_testing()

# Include ctest
include(CTest)

# Add google test direcotries
add_subdirectory(googletest)

# Include headers files
include_directories(
    include
)
# All source files
set(Sources
    src/Checkout.cpp
)

# Create the source code as library
add_library(${This} STATIC ${Sources}) 

# Add CMakeLists.txt in test directory
add_subdirectory(test)