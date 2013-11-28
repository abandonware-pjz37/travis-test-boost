cmake_minimum_required(VERSION 2.8.4)
project(boost)

find_package(Boost 1.53 REQUIRED)

include_directories(${Boost_INCLUDE_DIRS})
message("Boost directories: ${Boost_INCLUDE_DIRS}")

add_executable(test_bin "./test.cpp")

enable_testing()
add_test(A test_bin)
