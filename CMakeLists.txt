cmake_minimum_required(VERSION 3.10...3.27)
project(MyProject)

# Use dynamic linking (matches NixOS package)
set(SFML_STATIC_LIBRARIES OFF)

find_package(SFML 2.6 COMPONENTS graphics window system REQUIRED)

add_executable(app "LAB 7/main.cpp" "LAB 7/Objects.cpp")
target_link_libraries(app PRIVATE
    sfml-graphics
    sfml-window
    sfml-system
)

target_include_directories(app PRIVATE
    ${SFML_INCLUDE_DIR}
)