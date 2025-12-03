cmake_minimum_required(VERSION 4.2)
project(THULAC)

file(GLOB SOURCE_FILES include/*.h)
include_directories(${PROJECT_SOURCE_DIR}/include)


add_executable(thulac src/thulac.cc ${SOURCE_FILES})
add_executable(train src/train_c.cc ${SOURCE_FILES})
add_executable(test_case test/test_case.cpp ${SOURCE_FILES})
add_executable(thulac_test src/thulac_test.cc ${SOURCE_FILES})
