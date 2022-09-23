cmake_minimum_required (VERSION 3.0)
project (hashlib CXX)

add_library (hash-library
  md5.cpp
  md5.h
  )

target_compile_definitions(hash-library
  PUBLIC -DUNIVERSAL
  )

target_link_libraries(hash-library PUBLIC
  EndianPortable
  )

target_include_directories(hash-library PUBLIC
  ${PROJECT_SOURCE_DIR}
  )
