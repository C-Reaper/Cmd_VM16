# Project README

## Overview
This project is a C-based application that demonstrates the use of custom languages and libraries. It includes scripts written in a hypothetical custom language (.svm16, .lvm16), assembly code (.vm16), and uses various system libraries for different operating systems.

## Features
- Custom scripting languages (e.g., .svm16, .lvm16)
- Assembly code compilation (.vm16)
- Cross-platform build support (Linux, Windows, Wine, WebAssembly)

## Project Structure
The project structure is as follows:

### Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools
- Libraries needed for specific projects:
  - Linux: X11, PNG, JPEG
  - Windows: WINAPI
  - Wine: None (built-in support)
  - WebAssembly: Emscripten or wasmtime

## Build & Run
### Building the Project
To build the project on a Linux system, use:
```sh
cd <Project>
make -f Makefile.linux all
```
For Windows, use:
```sh
cd <Project>
make -f Makefile.windows all
```
For Wine cross-compilation for Windows, use:
```sh
cd <Project>
make -f Makefile.wine all
```
For WebAssembly using Emscripten or wasmtime, use:
```sh
cd <Project>
make -f Makefile.web all
```

### Running the Project
To run the compiled executable on Linux, use:
```sh
make -f Makefile.linux exe
```
On Windows, use:
```sh
make -f Makefile.windows exe
```
For Wine cross-compilation for Windows, use:
```sh
WINEPREFIX=~/wine64 WINEARCH=win64 wine <Project>/build/Main.exe
```
For WebAssembly using Emscripten or wasmtime, use:
```sh
wasmtime <Project>/build/Main.wasm
```

### Clean Build
To clean the build artifacts and rebuild the project:
```sh
make -f Makefile.linux clean
make -f Makefile.linux all
```
For Windows, use:
```sh
make -f Makefile.windows clean
make -f Makefile.windows all
```
For Wine cross-compilation for Windows, use:
```sh
make -f Makefile.wine clean
make -f Makefile.wine all
```
For WebAssembly using Emscripten or wasmtime, use:
```sh
make -f Makefile.web clean
make -f Makefile.web all
```