cmake_minimum_required(VERSION 4.2)
project(THULAC)

file(GLOB SOURCE_FILES include/*.h)
include_directories(${PROJECT_SOURCE_DIR}/include)

option(THULAC_BUILD_TARGET "Choose which target to build" "all")

add_executable(thulac src/thulac.cc ${SOURCE_FILES})
add_executable(thulac_train src/train_c.cc ${SOURCE_FILES})
add_executable(thulac_test_case test/test_case.cpp ${SOURCE_FILES})
add_executable(thulac_test src/thulac_test.cc ${SOURCE_FILES})

install(
  TARGETS thulac
  RUNTIME DESTINATION bin/
  LIBRARY DESTINATION lib/
  ARCHIVE DESTINATION lib/)



