cmake_minimum_required(VERSION 3.21)
project(detours)

include_directories(src)

set(SOURCES
	src/creatwth.cpp
	src/disolarm.cpp
	src/disolx64.cpp
	src/modules.cpp
	src/detours.cpp
	src/disolarm64.cpp
	src/disolx86.cpp
	src/disasm.cpp
	src/disolia64.cpp
	src/image.cpp
)

set(HEADERS
	src/detours.h
	src/detver.h
	src/uimports.cpp
)

set_property(SOURCE src/uimports.cpp APPEND PROPERTY HEADER_FILE_ONLY true)

add_library(${PROJECT_NAME} STATIC ${HEADERS} ${SOURCES})