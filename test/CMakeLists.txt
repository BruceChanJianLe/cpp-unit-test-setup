cmake_minimum_required(VERSION 3.8)

# Set local variable "This" as "CheckoutTest"
set(This CheckoutTest)

# All source files
set(Sources
    CheckoutTest.cpp
)

# Include headers files
include_directories(
    ../include
)

# Create CheckoutTests executable
add_executable(${This} ${Sources})
target_link_libraries(${This} PUBLIC
    gtest_main
    Checkout
)

# Run Unit Test
add_test(
    NAME ${This}
    COMMAND ${This}
)