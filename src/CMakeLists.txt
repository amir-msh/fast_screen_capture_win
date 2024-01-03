# The Flutter tooling requires that developers have CMake 3.10 or later
# installed. You should not increase this version, as doing so will cause
# the plugin to fail to compile for some customers of the plugin.
cmake_minimum_required(VERSION 3.10)

project(fast_screen_capture_win_library VERSION 0.0.1 LANGUAGES C)

add_library(fast_screen_capture_win SHARED
  "fast_screen_capture_win.c"
)

set_target_properties(fast_screen_capture_win PROPERTIES
  PUBLIC_HEADER fast_screen_capture_win.h
  OUTPUT_NAME "fast_screen_capture_win"
)

target_compile_definitions(fast_screen_capture_win PUBLIC DART_SHARED_LIB)
