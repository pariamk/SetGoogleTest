cmake_minimum_required(VERSION 3.5)
project(SettingUpGoogleTest)

set(CMAKE_CXX_STANDARD 11)

add_subdirectory(lib/googletest-master)
include_directories(lib/googletest-master/googletest/include)
include_directories(lib/googletest-master/googlemock/include )


set(SOURCE_FILES main.cpp lib/Test/Test.cpp lib/Test/className.h lib/Test/TDMASolver.h lib/Test/testTDMA.cpp )
add_executable(SettingUpGoogleTest ${SOURCE_FILES})
target_link_libraries(SettingUpGoogleTest gtest gtest_main)