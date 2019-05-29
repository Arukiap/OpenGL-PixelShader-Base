# OpenGL-Shaders-Base
A base openGL application written in C++ that sets you up for GLSL shader development in your machine. It is set up especially for fragment shader implementations such as the ones available at [Shader Toy](https://www.shadertoy.com/).

All the libraries are statically referenced and included in this repository for ease of use.

## Building on Linux

### Dependencies

- Make sure you have the latest legacy drivers installed for you graphics card.

Install the following dependencies on your machine:

**SDL2** - *Cross-platform development library designed to provide low level access to audio, keyboard, mouse, joystick, and graphics hardware via OpenGL and Direct3D*
```
sudo apt-get install libsdl2-dev
```

**GLEW** - OpenGL extension manager
```
sudo apt-get install libglew-dev
```

### Compiling and Running

If you are using Visual Studio Code, it is as simple as pressing Ctrl + Shift + B to run the compilation and run tasks consecutively.

To compile:
```
g++ -g \*.cpp -I include/ -Llib -lGLEW -lSDL2main -lSDL2 -o main.cpp.out -lOpenGL
```
To run:
```
./main.cpp.out
```

## Building on Windows

### Dlls and Mingw

In order to build this base application on windows you need to first move the files in the `dlls` directory to the root folder of the application.

You also need to install the mingw compiler in your machine and set its `bin` folder path on the global environment PATH variable.

### Compiling and Running

You are now ready to compile and run the application. If you are using Visual Studio Code, there is already a task available that compiles and runs the code consecutively if you press the Ctrl + Shift + B key combination inside VScode.

If you are using another code editor, please refer to the next commands (assuming you are running windows powershell):

To compile:
```
g++ -g \*.cpp -I include\\ -Llib -lglew32s -lSDL2main -lSDL2 -o main.cpp.exe -lopengl32
```
To run:
```
.\\main.cpp.exe
```

# How do I know if it is working?

If a windows opens up flashing between blue and purple color you know it is working.
