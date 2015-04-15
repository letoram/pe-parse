cmake_minimum_required (VERSION 2.8)
project (pe-parse)

add_subdirectory(parser-library)

if (CMAKE_BUILD_TYPE STREQUAL "Debug")
	add_subdirectory(dump-prog)
endif()
