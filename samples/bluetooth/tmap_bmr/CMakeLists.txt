# SPDX-License-Identifier: Apache-2.0

cmake_minimum_required(VERSION 3.20.0)
find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
project(tmap_bmr)

target_sources(app PRIVATE
  src/main.c
  src/vcp_vol_renderer.c
  src/bap_broadcast_sink.c
)

zephyr_library_include_directories(${ZEPHYR_BASE}/samples/bluetooth)
