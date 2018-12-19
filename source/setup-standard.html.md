---
title: Standard Configuration

language_tabs:

toc_footers:

includes:

search: true
---

# Standard Configuration

## What You Need

 * [CMake](https://cmake.org/download/)
 * OpenSSL library
   * For Windows users, you can [Download and use the installer (Don't download the light version or you'll run into errors)](https://slproweb.com/products/Win32OpenSSL.html) or any other binaries [found here](https://wiki.openssl.org/index.php/Binaries) or [via a simple google search](https://www.google.com/search?q=openssl+windows+precompiled).
   * For Linux users, use your package manager and install libssl-dev or openssl-devel. The name depends on your package manager.
 * A C++ Compiler
   * [Go here for build status](https://github.com/yourWaifu/sleepy-discord#build-status).
   * For Visual Studio users, Visual Studio has a c++ compiler.

## Instructions

### Configuring CMake

```cmake
#CMakeLists.txt
cmake_minimum_required (VERSION 3.6)
project(example)

add_executable(replace-me source.cpp)
```

```cmake
#Add these two lines
add_subdirectory(path/to/sleepy-discord)
target_link_libraries(replace-me sleepy-discord)
```

 1. In case you haven't already created a CMakeLists.txt for your project. please do so on the root directory or folder of your project.

 2. Replace replace-me with the name of your project or executable.

 3. Add these two lines to the CMakeList.txt so that Sleepy Discord will be linked.

 4. Replace path/to/sleepy-discord with the relative path to the sleepy-discord directory or folder. Also remember to replace replace-me with the name of your executable.

## Next Step

Using CMake to Generate build configuration files.

 * [CMake Graphical User Interface (GUI)](setup-standard-gui)
 * [CMake Command line Interface (CLI)](setup-standard-cli)
 * [Visual Studio CMake](setup-standard-vs-cmake)