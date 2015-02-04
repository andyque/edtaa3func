cmake_minimum_required(VERSION 2.8)

project (edtaa3func)

set(edtaa3func_SRC
./edtaa3func.cpp
)

include_directories(
  ${CMAKE_CURRENT_SOURCE_DIR}
)

add_library(edtaa3func STATIC
  ${edtaa3func_SRC}
)

set_target_properties(edtaa3func
    PROPERTIES
    ARCHIVE_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib"
    LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib"
)
#install header files
install(DIRECTORY . DESTINATION "include/"
  FILES_MATCHING PATTERN "*.h") 
