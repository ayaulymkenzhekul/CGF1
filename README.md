# CGF1 - Assignment 1

# CGF1 — Task 1: Red Triangle and Blue Square OpenGL Programs

## Project Description
This project contains two simple OpenGL programs:

1. **red_triangle.exe**  
   - Initially draws a red triangle.  
   - Modified version draws a blue square that fits inside the window.

2. **blue_square.exe**  
   - Draws a blue square inside the window.

The project is written in C++ using the following libraries:
- OpenGL
- GLFW
- GLEW

CMake is used for building the project.

## Requirements
- Windows 10 or higher
- Visual Studio 2022
- CMake 3.8 or higher
- vcpkg package manager

## Installing Dependencies
1. Open a terminal and go to the vcpkg folder.
2. Install required libraries:

vcpkg install glfw3:x64-windows glew:x64-windows

(Linux/Ubuntu)

   sudo apt-get update
   sudo apt-get install cmake g++ libglfw3-dev libglew-dev libglm-dev

3. Integrate vcpkg with Visual Studio:

vcpkg integrate install


## Building the Project
1. Open a terminal and go to the project folder.
2. Generate build files using CMake:

cmake -B build -S . -DCMAKE_TOOLCHAIN_FILE=C:/vcpkg/scripts/buildsystems/vcpkg.cmake



3. Build the project:

cmake --build build



> After building, executable files will be located in `build/Debug/`.

## Running the Programs
- Run the red triangle / modified blue square:

build/Debug/red_triangle.exe



- Run the blue square:

build/Debug/blue_square.exe



## Project Structure

CGF1/
├─ CMakeLists.txt
├─ CGF1.cpp
├─ CGF1.h
├─ red_triangle.cpp
├─ blue_square.cpp
├─ README.md
└─ build/

