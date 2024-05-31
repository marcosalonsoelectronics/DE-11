cmake_minimum_required(VERSION 3.12)

# Pull in SDK (must be before project)
include(pico_sdk_import.cmake)

project(blink-led)

# Initialize the SDK
pico_sdk_init()

add_executable(blink-led blink-led.c)

# pull in common dependencies
target_link_libraries(blink-led pico_stdlib)

# create map/bin/hex file etc.
pico_add_extra_outputs(blink-led)

