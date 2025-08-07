cmake_minimum_required(VERSION 3.13)

# initialize the SDK based on PICO_SDK_PATH
# note: this must happen before project()
include(pico_sdk_import.cmake)

project(my_project)

# initialize the Raspberry Pi Pico SDK
pico_sdk_init()

# rest of your project
add_executable(my_project
    main.c
)

# link the executable to the Pico standard library
target_link_libraries(my_project pico_stdlib)

pico_add_extra_outputs(my_project)

include_directories(
    /usr/arm-none-eabi/include
    /usr/lib/gcc/arm-none-eabi/14.2.0/include
    /usr/lib/gcc/arm-none-eabi/14.2.0/include-fixed
)

