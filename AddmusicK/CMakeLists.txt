# 3.8 is the first version to support C++17
cmake_minimum_required(VERSION 3.8)

set(CMAKE_CXX_STANDARD 17)

file(GLOB SOURCES *.cpp MML/*.cpp MML/Lexers/*.cpp Music/*.cpp Binary/*.cpp ../AM405Remover/AddMusic.cpp asardll.c)
set_source_files_properties(asardll.c PROPERTIES LANGUAGE CXX)
add_executable(addmusick ${SOURCES})
# TODO: make this system/compiler-agnostic
target_link_libraries(addmusick stdc++fs dl)
