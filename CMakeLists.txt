cmake_minimum_required(VERSION 2.8)

project (edtaa3func)

set(SRC
./edtaa3func.cpp
)

include_directories(
  ${CMAKE_CURRENT_SOURCE_DIR}
)

add_library(edtaa3func STATIC
  ${SRC}
)

INSTALL(
  TARGETS edtaa3func
  ARCHIVE DESTINATION lib
  LIBRARY DESTINATION lib
  COMPONENT library
)

INSTALL(FILES edtaa3func.h
        DESTINATION "include"
)
