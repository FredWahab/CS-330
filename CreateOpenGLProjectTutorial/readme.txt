How to create a new OpenGL project. (included files for windows users only)

1. open visual studio and create new empty c++ project.

2. create a main.cpp file, copy the sample code into the file and debug. 
(this is to initialize the files and folders)

#include <iostream>

int main() {
    std::cout << "Hello, OpenGL!" << std::endl;
    return 0;
}

3. drop the included dependencies folder into your project folder. 
Refresh in visual studio. (properties -> show in explorer) 
select the include and lib folder and include in project. 

4. replace the previous sample code with the code from GLFW to verify correct setup. 
https://www.glfw.org/documentation.html 
(errors will appear at first)

5. go to properties -> c/c++ -> general -> additional include directories and add the include folder

6. go to properties -> linker -> general -> additional library directories and add the lib folder

7. go to properties -> linker -> input -> additional dependencies and add the following files
glfw3.lib
opengl32.lib
user32.lib
gdi32.lib
shell32.lib

8. drop the included glad.c file into your project folder.
select the glad.c file in visual studeio and include in project

9. select build -> clear solution and then rebuild solution. 
all errors should clear and the project should sucessfully run. 
