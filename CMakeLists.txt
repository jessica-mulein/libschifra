cmake_minimum_required (VERSION 2.8)
cmake_policy(SET CMP0054 OLD)

project ("Schiffra RS LIB")
set(CMAKE_BUILD_TYPE Release)
option(BUILD_EXAMPLES "Compile the examples" OFF)

if (NOT ${CMAKE_CXX_COMPILER_ID} STREQUAL "MSVC")
    set(CMAKE_CXX_FLAGS "--std=c++11 -pthread ${CMAKE_CXX_FLAGS}")
endif()

include_directories(include)
enable_testing()
add_subdirectory(tests)
if(BUILD_EXAMPLES)
  add_subdirectory(examples)
endif(BUILD_EXAMPLES)

file(GLOB files "${CMAKE_SOURCE_DIR}/include/*")
install(FILES ${files} DESTINATION include)
