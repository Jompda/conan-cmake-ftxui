cmake_minimum_required(VERSION 3.15)

project(testing LANGUAGES CXX VERSION 1.0.0)

find_package(ftxui 5 REQUIRED)

add_executable(${PROJECT_NAME} src/main.cpp)
target_link_libraries(${PROJECT_NAME}
	PRIVATE ftxui::screen
	PRIVATE ftxui::dom
	PRIVATE ftxui::component
)

