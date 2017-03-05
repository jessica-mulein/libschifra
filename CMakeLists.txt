cmake_minimum_required (VERSION 2.8)
cmake_policy(SET CMP0054 OLD)

project ("Schiffra RS LIB")
set(CMAKE_BUILD_TYPE Release)
option(COMPILE_EXAMPLES "Compile the examples" ON)

if (NOT ${CMAKE_CXX_COMPILER_ID} STREQUAL "MSVC")
    set(CMAKE_CXX_FLAGS "--std=c++11 -pthread ${CMAKE_CXX_FLAGS}")
endif()

include_directories(include)
add_subdirectory(tests)
if(COMPILE_EXAMPLES)
  add_subdirectory(examples)
endif(COMPILE_EXAMPLES)

FILE(GLOB files "${CMAKE_SOURCE_DIR}/include/*")
MESSAGE(STATUS "FILES: " ${files})
install(FILES ${files} DESTINATION include)
