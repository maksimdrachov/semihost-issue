# SPDX-License-Identifier: Apache-2.0

cmake_minimum_required(VERSION 3.20.0)
# Re-direct the directory where the 'boards' directory is found from
# $ZEPHYR_BASE to this directory.
set(BOARD_ROOT ${CMAKE_CURRENT_LIST_DIR}/../../../epm)
find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
project(semihost)

FILE(GLOB app_sources src/*.c)
target_sources(app PRIVATE ${app_sources})
