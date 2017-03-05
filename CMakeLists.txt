cmake_minimum_required (VERSION 2.8)
project ("Schiffra RS LIB")
set(CMAKE_BUILD_TYPE Release)
option(COMPILE_EXAMPLES "Compile the examples" ON)


if(CMAKE_COMPILER_IS_GNUCC)
  # #set(CMAKE_CXX_COMPILER "/usr/bin/clang++")
   set(CMAKE_CXX_FLAGS "--std=c++11 -pthread ${CMAKE_CXX_FLAGS}")
endif(CMAKE_COMPILER_IS_GNUCC)

include_directories(include)
add_subdirectory(tests)
if(COMPILE_EXAMPLES)
  add_subdirectory(examples)
endif(COMPILE_EXAMPLES)

FILE(GLOB files "${CMAKE_SOURCE_DIR}/include/*")
MESSAGE(STATUS "FILES: " ${files})
install(FILES ${files} DESTINATION include)
