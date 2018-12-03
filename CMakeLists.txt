cmake_minimum_required(VERSION 3.13)

project(DXRFallbackLayer)

file(GLOB_RECURSE SOURCES CONFIGURE_DEPENDS "src/*.cpp")
file(GLOB_RECURSE HEADERS CONFIGURE_DEPENDS "src/*.h")

ADD_DEFINITIONS(-DUNICODE)
ADD_DEFINITIONS(-D_UNICODE)

include_directories(WispDemo Include)
add_library(WispDemo ${HEADERS} ${SOURCES})
target_link_libraries(WispDemo d3d12)
