
set(SRCROOT ${PROJECT_SOURCE_DIR}/examples/pong)

project(pong)

add_executable(${PROJECT_NAME})

target_sources(${PROJECT_NAME} PRIVATE
	Pong.cpp
)

find_package(SFML CONFIG REQUIRED COMPONENTS audio graphics)

target_link_libraries(${PROJECT_NAME} PRIVATE
	sfml-audio
	sfml-graphics
)

project_install_target()
project_compile_options()
