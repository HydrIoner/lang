# CMakeList.txt: src 的 CMake 项目，在此处包括源代码并定义
# 项目特定的逻辑。
cmake_minimum_required (VERSION 3.8)
# 将源代码添加到此项目的可执行文件。
aux_source_directory(. DIR_SRC)

add_subdirectory(helpers)

add_executable (lang ${DIR_SRC})

target_link_libraries(lang helpers)