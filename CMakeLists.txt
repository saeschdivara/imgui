cmake_minimum_required(VERSION 3.20)
project(imgui)

if (${CMAKE_SYSTEM_NAME} MATCHES "Windows")
    add_library(imgui STATIC
            imgui.cpp
            imgui_draw.cpp
            imgui_tables.cpp
            imgui_widgets.cpp
            imgui_demo.cpp
    )

    add_library(imgui_extra STATIC
            misc/cpp/imgui_stdlib.cpp
    )

else()
    add_library(imgui SHARED
            imgui.cpp
            imgui_draw.cpp
            imgui_tables.cpp
            imgui_widgets.cpp
            imgui_demo.cpp
            )

    add_library(imgui_extra SHARED
            misc/cpp/imgui_stdlib.cpp
    )
endif()