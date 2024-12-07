project(ImGui)

file(GLOB IMGUI_SRCS "*.cpp")
file(GLOB IMGUI_HDRS "*.h")

add_library(
    ${PROJECT_NAME} STATIC
    "imgui_demo.cpp"
    "imgui_draw.cpp"
    "imgui_tables.cpp"
    "imgui_widgets.cpp"
    "imgui.cpp"
    ${IMGUI_HDRS}
)

target_include_directories(${PROJECT_NAME} PUBLIC ".")
target_include_directories(${PROJECT_NAME} PUBLIC "backends")
