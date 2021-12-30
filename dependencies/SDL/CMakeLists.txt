include(FetchContent)

FetchContent_Declare(
	SDL
	GIT_REPOSITORY https://github.com/libsdl-org/SDL.git
	#GIT_TAG 2.0.18
)

FetchContent_MakeAvailable(SDL)