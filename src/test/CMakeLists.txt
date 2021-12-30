add_executable(
	opengl_test
	main_test.cpp
)
target_link_libraries(
	opengl_test PRIVATE
	jsoncpp_static
	libglew_static
	glfw
)
target_include_directories(opengl_test PUBLIC "${PROJECT_SOURCE_DIR}/include")
target_include_directories(opengl_test PUBLIC ${PROJECT_SOURCE_DIR}/glfw/include)
target_include_directories(opengl_test PUBLIC ${PROJECT_SOURCE_DIR}/glew/include)

add_custom_command(
	TARGET opengl_test
	COMMAND ${CMAKE_COMMAND} -E copy_directory
		${PROJECT_SOURCE_DIR}/shaders $<TARGET_FILE_DIR:opengl_test>/shaders
)


add_test(NAME OpenGLTest COMMAND opengl_test)