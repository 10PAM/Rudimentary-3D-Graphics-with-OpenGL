# Rudimentary 3D Graphics With OpenGL
Understanding 3D Graphics with OpenGL.

# 3D Graphics with OpenGL: Setting Up and Understanding the Environment
Provided to you by: Mario Aguilera Piceno

## Understanding Compiling
- Compiling is the process of: compilation.
- It takes all source code files (C, C++, headers) and checks for code definitions and proper programming syntax (Does not check for runtime errors)
- It creates an executable file using all provided source files

## Compilation Process Overview (C, C++):
1. Compiler gets takes in any provided source code: C or C++ (.c, .h, .cpp, .hpp)
2. Preprocessing: Preprocessor handles all lines starting with "#" (i.e. #include, #define) from included files, it expands on macros, and manages conditional compilation (#ifdef, etc.). This creates a .i file and passes it to the compiler
3. Compilation: Compiler translates C++ code into assembly and evaluates syntax and converts to assembly code (.s file)
4. Assembly: Assembler converts assembly code into object code, creating a binary file (.o file)
5. Linking: Linker compiles any provided object files and links static and or dynamic libraries (.lib - Windows; .a - Linux; .ar - Linux)
6. Executing: final object executable file can be called using ./<filename>

### Diagram Example of Compilation Process Pipeline (C, C++):
<img width="826" height="359" alt="image" src="https://github.com/user-attachments/assets/5fcd56eb-4b7c-4e13-8b6b-6dd5b17212f9" />
