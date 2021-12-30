# CMakeList.txt : 最上位の CMake プロジェクト ファイル。グローバル構成を行います
# また、サブプロジェクトをここに含めます。
#
cmake_minimum_required (VERSION 3.8)

project ("WanderTypingGame")

# add_subdirectory(dependencies/SDL)
add_subdirectory(glew)
add_subdirectory(glfw)
add_subdirectory(dependencies/json-cpp)


option(WANDER_WITH_TEST "Build and run RileyJsonCppUtils test executables" ON)

# add_subdirectory(src/main)

if (${WANDER_WITH_TEST})
	enable_testing()
	add_subdirectory(src/test)
	# add_subdirectory(src/test/wander_tests)
endif()
