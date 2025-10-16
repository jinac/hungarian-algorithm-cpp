cmake_minimum_required(VERSION 3.10)
project(hungarian-algorithm-cpp)

add_library(hungarian Hungarian.cpp Hungarian.h)
target_include_directories(hungarian PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
target_compile_features(hungarian PUBLIC cxx_std_11)

# Optional: test executable
add_executable(hungarian_test testMain.cpp)
target_link_libraries(hungarian_test PRIVATE hungarian)
