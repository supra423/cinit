# Introduction
`cinit` (pronounced "sinit") is just a very small script I made to help me with other C/C++ projects.
It is a simple script that will initialize a new C/C++ project within the current directory
that includes a basic structure and a makefile.

# Requirements
- The Linux distribution of your choice (ofc)
- bash 
- make
- git
- bear 
- C/C++ compiler (preferably gcc/g++)

# Usage
1. Clone the repository:
```bash
git clone https://github.com/supra423/cinit.git
```
2. Navigate to the directory:
```bash
cd cinit
```
3. Make the script executable: (The script is already executable, but just in case)
```bash
chmod +x cinit
```
4. Run the script to test (make sure you are in the directory where the script is located):
```bash
./cinit
```
5. (Optional) Copy the script to a directory in your PATH for easier access:
```bash
sudo cp cinit -r /usr/bin/
```
6. Now you can run the script from anywhere:
```bash
cinit c
```
or
```bash
cinit cpp
```
# Note
- Do note that this script is meant to be run in an empty directory where you want to create your project.
There is still no feature that makes it create a new directory for the project, so you have to `mkdir` 
the directory yourself, `cd` to it, and then run the script inside it.
- `sh` may work but you would have to change the shebang from `#!/usr/bin/bash` to `#!/bin/sh`
- This initializes a git repository in the project directory.
- The makefile is set up to use gcc/g++. If you want to use clang,
you will need to modify the makefile template accordingly.
- The script will create a basic structure for your project, including
    * an include directory for header files,
    * a bin directory for the binaries,
    * an obj directory for the object files, (not yet linked)
    * src directory for the main.c or main.cpp file depending on the language you choose.
    * compile_commands.json created by bear to make LSPs work properly.
    * and a makefile for automation of the build process.
- This script is NOT meant to be used for production projects, but rather as a starting
point for small projects or for learning purposes. I personally made this script just for ME.

# Contributing
If you have any suggestions or improvements, feel free to open an issue or a pull request.
Do mind that this script is just a personal project and is definitely not suitable for all use cases,
so I may not accept all contributions.
