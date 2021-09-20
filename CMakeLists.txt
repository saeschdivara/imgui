cmake_minimum_required(VERSION 3.20)
project(imgui)

add_library(imgui SHARED
        imgui.cpp
        imgui_draw.cpp
        imgui_tables.cpp
        imgui_widgets.cpp
)