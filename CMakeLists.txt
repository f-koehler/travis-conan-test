cmake_minimum_required(VERSION 2.8)
project(travis-conan-test)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()
find_package(Boost REQUIRED COMPONENTS program_options)

add_executable(main main.cpp)
target_link_libraries(main ${Boost_LIBRARIES})
