set(SOURCES buffer.cpp parse.cpp)
add_definitions(-std=c++11)

add_library(pe_parser-static STATIC ${SOURCES})
add_library(pe_parser SHARED ${SOURCES})

install(TARGETS pe_parser pe_parser-static
	LIBRARY DESTINATION lib
	ARCHIVE DESTINATION lib)

install(FILES nt-headers.h parse.h to_string.h DESTINATION include/pe_parser)
