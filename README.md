# Installation
## Ubntu18.04
```bash
$ cd ~
$ git clone --recursive https://github.com/GodRyosuke/WanderTypingGame.git
$ cd WanderTypingGame
$ mkdir build && cd build
$ cmake ..
$ make
$ cd src/test
$ ./opengl_test
```

## Windows10
push the 'windows key', and type 'cmd'. Aafter that, you can see the comand prompt is up.
Then, type these commands below.
#### Attention!!
You need MinGW to build this project!!
So, please install MinGW before cmake if you haven't install it yet.

```bash
> cd path\to\your\cloning\dir
> git clone --recursive https://github.com/GodRyosuke/WanderTypingGame.git
> cd WanderTypingGame
> mkdir build
> cd build
> cmake -G "MinGW Makefiles" -S ../ -B .
> cmake --build .
> cd src\test
> opengl_test.exe
```

# Links for References

https://www.youtube.com/watch?v=Nzp77cOMmfg
