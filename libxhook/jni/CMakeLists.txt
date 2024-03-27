cmake_minimum_required(VERSION 3.22.1)
project(xhook)

set(CMAKE_C_STANDARD 11)

add_library(xhook SHARED
        xhook.c
        xh_core.c
        xh_elf.c
        xh_jni.c
        xh_log.c
        xh_util.c
        xh_version.c
)

target_include_directories(
        xhook
        PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}
)

target_link_libraries(
        xhook PUBLIC
        log
)
