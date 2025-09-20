cmake_minimum_required(VERSION 3.30)
#PICO SDK
include(../pico-sdk/external/pico_sdk_import.cmake)

project(blink C CXX ASM)
set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)

#Init SDK
pico_sdk_init()

add_executable(blink
  blink.c
  )

target_link_libraries(blink pico_stdlib)

#for uf2
pico_add_extra_outputs(blink)
