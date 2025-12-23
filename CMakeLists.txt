cmake_minimum_required(VERSION 3.13)
set(CMAKE_INCLUDE_CURRENT_DIR ON)
include(pico_sdk_import.cmake)
project(qtpy2040_serprog)

pico_sdk_init()

add_executable(qtpy2040_serprog)
target_sources(qtpy2040_serprog PRIVATE main.c usb_descriptors.c)
target_link_libraries(qtpy2040_serprog PRIVATE pico_stdlib pico_unique_id hardware_spi tinyusb_device)
pico_add_extra_outputs(qtpy2040_serprog)
