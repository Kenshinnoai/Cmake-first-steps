project(MyProgram)

#we tell CMake in addition to create .lib and some more libraries required for creating .dll library
SET(CMAKE_WINDOWS_EXPORT_ALL_SYMBOLS ON)

#look carefully, I added "SHARED" to MyLib to make it not .lib, but .dll (normally all libraries have STATIC type) 
add_executable(MyExe main.c)
add_library(MyLib SHARED MyLib.c)

target_link_libraries(MyExe MyLib)
