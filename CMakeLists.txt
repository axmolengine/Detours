cmake_minimum_required(VERSION 3.27...4.2)

project(detours)

set(detours_SOURCE_FIELS
  src/detours.cpp
  src/modules.cpp
  src/disasm.cpp
  src/image.cpp
  src/creatwth.cpp
  src/disolx86.cpp
  src/disolx64.cpp
  src/disolia64.cpp
  src/disolarm.cpp
  src/disolarm64.cpp
)


add_library(detours STATIC ${detours_SOURCE_FIELS})

target_compile_definitions(detours
  PUBLIC WIN32_LEAN_AND_MEAN=1
  PUBLIC _WIN32_WINNT=0x601
)

target_include_directories(detours INTERFACE ${CMAKE_CURRENT_LIST_DIR}/src)
