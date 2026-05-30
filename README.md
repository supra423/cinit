# Introduction
This is just a very small script I made to help me with other C/C++ projects.
It is a simple script that will initialize a new C/C++ project within the current directory
that includes a basic structure and a makefile.

# Requirements
- A Linux distribution (ofc)
- bash
- make
- git
- bear
- gcc and g++ (clang works but you have to manually change the makefile)

# Usage
1. Clone the repository:
```bash
git clone https://github.com/supra423/C_initscript.git
```
2. Navigate to the directory:
```bash
cd C_initscript
```
3. Make the script executable: (The script is already executable, but just in case)
```bash
chmod +x initscript
```
4. Run the script to test (make sure you are in the directory where the script is located):
```bash
./initscript
```
5. (Optional) Copy the script to a directory in your PATH for easier access:
```bash
sudo cp init.sh -r /usr/local/bin/
```
6. Now you can run the script from anywhere:
```bash
initscript c
```
or
```bash
initscript cpp
```
# Note
- Do note that this script is meant to be run in an empty directory where you want to create your project.
There is still no feature that makes it create a new directory for the project, so you have to `mkdir` 
the directory yourself, `cd` to it, and then run the script inside it.
- This initializes a git repository in the project directory.
- The makefile is set up to use gcc and g++. If you want to use clang,
you will need to modify the makefile accordingly.
- The script will create a basic structure for your project, including
    * an include directory for header files,
    * a bin directory for the binaries,
    * an obj directory for the object files, (not yet linked)
    * src directory for the main.c or main.cpp file depending on the language you choose.
    * compile_commands.json created by bear to make LSPs work properly.
    * and a makefile for automation of the build process.
- This script is NOT meant to be used for production projects, but rather as a starting
point for small projects or for learning purposes. I personally made this script just for ME.


