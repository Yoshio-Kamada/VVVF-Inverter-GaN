# Generated Cmake Pico project file

cmake_minimum_required(VERSION 3.13)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# Initialise pico_sdk from installed location
# (note this can come from environment, CMake cache etc)

# == DO NOT EDIT THE FOLLOWING LINES for the Raspberry Pi Pico VS Code Extension to work ==
if(WIN32)
    set(USERHOME $ENV{USERPROFILE})
else()
    set(USERHOME $ENV{HOME})
endif()
set(sdkVersion 2.2.0)
set(toolchainVersion RISCV_ZCB_RPI_2_1_1_3)
set(picotoolVersion 2.2.0)
set(picoVscode ${USERHOME}/.pico-sdk/cmake/pico-vscode.cmake)
if (EXISTS ${picoVscode})
    include(${picoVscode})
endif()
# ====================================================================================
set(PICO_BOARD pico2 CACHE STRING "Board type")

# Pull in Raspberry Pi Pico SDK (must be before project)
include(pico_sdk_import.cmake)

project(vvvvfinverter C CXX ASM)

# Initialise the Raspberry Pi Pico SDK
pico_sdk_init()

# Add executable. Default name is the project name, version 0.1

add_executable(vvvvfinverter vvvvfinverter.cpp )

pico_set_program_name(vvvvfinverter "vvvvfinverter")
pico_set_program_version(vvvvfinverter "0.1")

# Modify the below lines to enable/disable output over UART/USB
pico_enable_stdio_uart(vvvvfinverter 1)
pico_enable_stdio_usb(vvvvfinverter 0)

# Add the standard library to the build
target_link_libraries(vvvvfinverter
        pico_stdlib
        hardware_adc
        hardware_gpio
        hardware_clocks)

# Add the standard include files to the build
target_include_directories(vvvvfinverter PRIVATE
        ${CMAKE_CURRENT_LIST_DIR}
)

pico_add_extra_outputs(vvvvfinverter)

target_link_libraries(vvvvfinverter
    pico_stdlib
    hardware_adc
    hardware_gpio
)
# Add the pico-sdk libraries to the build
