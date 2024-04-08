#choose needed version of CMake to everything worked correctly (I've chosen the most recommended in YouTube)
cmake_minimum_required(VERSION 3.2)

#declare your project's name (any) 
project(MyProgram)

#adding two tasks to linker: to make .exe file of main.c and create STATIC library of MyLib.c
#MyExe and MyLib are both alias for files on the right of it  
add_executable(MyExe main.c)
add_library(MyLib MyLib.c)

#link main.c and MyLib.c files to make MyLib code visible for main.c code
target_link_libraries(MyExe MyLib)
