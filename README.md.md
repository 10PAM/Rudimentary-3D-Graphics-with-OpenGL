1 

3D Graphic with OpenGL: Setting Up and Understanding the Environment 

Provided to You By: Mario Aguilera Piceno 



<!-- Start of picture text -->
2<br><!-- End of picture text -->



<!-- Start of picture text -->
Understanding Compiling<br>Understanding Compiling<br><!-- End of picture text -->

- 



<!-- Start of picture text -->
Compiling is the process of: compilation. Compiling is the process of: compilation.<br><!-- End of picture text -->

- 



<!-- Start of picture text -->
files, etc.) and looks for code definitions and  files, etc.) and Looks for code definitions and<br><!-- End of picture text -->

- 



<!-- Start of picture text -->
runtime errors usually  runtime errors usually –  —<br><!-- End of picture text -->



<!-- Start of picture text -->
compiler dependent). compiler dependent).<br><!-- End of picture text -->



<!-- Start of picture text -->
It creates an executable file using all provided  It creates an executable file using all provided<br><!-- End of picture text -->

3 

Understanding Compilation Process: C, C++ 

1. Source code: (C/C++ code written by programmer), .c, .h . files cpp , . hpp 

2. Preprocessing: Preprocessor handles all lines starting with # (i.e. #include, #define), and replaces them with code from the included files, it expands on macros, and manages conditional compilation (#ifdef, etc.). This creates a . i file and passes to compiler 

3. Compilation: Compiler translates C++ code into assembly and evaluates syntax and converts to assembly code (.s file) 

4. Assembly: Assembler converts assembly code into object code, creating binary file (.o file) 

5. Linking: Linker compiles any provided object files and links libraries (.h, . hpp ) to create an executable (looks for main() method) 6. Executing: final object executable file can be called using ./<file> 



<!-- Start of picture text -->
Understanding Compilation Process: C,<br>Understanding Compilation Process: C,<br><!-- End of picture text -->



<!-- Start of picture text -->
4<br><!-- End of picture text -->







<mark>Source Preprocessor (.i) Compiler (.s) Assembler (.o, .obj) Linker  (.exe, .out) Executable</mark> 



<!-- Start of picture text -->
.c, . -C,<br><!-- End of picture text -->



<!-- Start of picture text -->
, .h, . h,<br><!-- End of picture text -->



<!-- Start of picture text -->
Expands macros, include headers<br>EXPands macros, include headers<br><!-- End of picture text -->



<!-- Start of picture text -->
-<br>Generates architecture<br>Generates architecture-specific<br><!-- End of picture text -->



<!-- Start of picture text -->
specific assembly<br>assembly<br><!-- End of picture text -->



<!-- Start of picture text -->
Converts machine code to Object files<br>COnverts machine code to Object files<br><!-- End of picture text -->



<!-- Start of picture text -->
Combines objects and libraries into<br>Combines, objects and libraries into<br><!-- End of picture text -->



<!-- Start of picture text -->
./<filename> . /<filename><br><!-- End of picture text -->

5 

Typical Compilation Errors - 1. Pre processing: Header not found, macro errors 2. Compilation: Syntax errors, type mismatches 3. Assembly: Architecture errors 4. Linking: Undefined references, missing symbols 5. Execution: Segmentation faults, logic bugs 



<!-- Start of picture text -->
6<br><!-- End of picture text -->



<!-- Start of picture text -->
-<br>Understanding Dynamic-Linked<br>Understanding Dynamic<br><!-- End of picture text -->



<!-- Start of picture text -->
Linked Libraries  Libraries<br><!-- End of picture text -->



<!-- Start of picture text -->
Contains compiled code loaded and executed at  Contains compiled code loaded and executed at<br><!-- End of picture text -->

• 



<!-- Start of picture text -->
File extension (Windows): . File extension (Windows): dll<br><!-- End of picture text -->

• 



<!-- Start of picture text -->
7<br><!-- End of picture text -->



<!-- Start of picture text -->
Understanding Static Libraries<br><!-- End of picture text -->

- 

- 



<!-- Start of picture text -->
These are used at compile/link time<br><!-- End of picture text -->



<!-- Start of picture text -->
Can contain compiled code (static library) or be a<br><!-- End of picture text -->



<!-- Start of picture text -->
that methods are referenced (i.e. prior to linking<br><!-- End of picture text -->

- 



<!-- Start of picture text -->
serve as a placeholder for accessing methods after<br><!-- End of picture text -->



<!-- Start of picture text -->
methods used need to be acknowledged, so methods do<br><!-- End of picture text -->



<!-- Start of picture text -->
8<br><!-- End of picture text -->



<!-- Start of picture text -->
Understanding Static Libraries. . .<br>Understanding Static Libraries. . .<br><!-- End of picture text -->

• 

• 

• 



<!-- Start of picture text -->
Problems: Whole app needs to be recompiled to  Problems: Whole app needs to be recompiled to<br><!-- End of picture text -->



<!-- Start of picture text -->
File extensions (Static): .lib (Windows), .a  File extensions (Static): .lib (Windows), .a<br><!-- End of picture text -->



<!-- Start of picture text -->
File extensions (Import): .lib (Windows), .so  File extensions (Import): .lib (Windows), .so<br><!-- End of picture text -->



<!-- Start of picture text -->
9<br><!-- End of picture text -->



<!-- Start of picture text -->
Understanding Compilers<br>Understanding Compilers<br><!-- End of picture text -->

• 



<!-- Start of picture text -->
MinGW (A C language) compiler that supports C++  MinGW (A C Language) compiler that supports C+<br><!-- End of picture text -->



<!-- Start of picture text -->
projects projects<br><!-- End of picture text -->

- 



<!-- Start of picture text -->
MSVC (Microsoft Visual C++) is a C and CH<br>MSVC (Microsoft Visual C++) is a C and C++<br><!-- End of picture text -->



<!-- Start of picture text -->
compiling almost any software application hosted  compiling almost any software application hosted<br><!-- End of picture text -->



<!-- Start of picture text -->
10<br><!-- End of picture text -->



<!-- Start of picture text -->
Getting Started<br><!-- End of picture text -->

- Software we will use: 

   - Visual Studio 

- Libraries we Will Use: 

   - GLEW (OpenGL Extension Wrangler Library): https://github.com/nigelscom/glew 

   - GLFW (OpenGL FrameWork): https://github.com/glfw/glfw 

   - GLM (OpenGL Mathematics): https://github.com/g-truc/glm 

   - SOIL2 (Simple OpenGL Image Library): https://github.com/SpartanJ/soil2 



<!-- Start of picture text -->
11<br><!-- End of picture text -->



<!-- Start of picture text -->
Understanding the Essentials (C, C++)<br><!-- End of picture text -->

- C: 

   - Created in 1972-1973 by Dennis Ritchie, who was working at AT&T Bell Laboratories 

   - • A programming language made to provide a high-level (less writing, more understanding) programming language that can provide low-level access to hardware. Alternative to assembly (second-gen language, made to replace binary coding) 

   - This language forms the basis for many modern computer operating systems today. 

- C++: 

   - Created by Bjarne Stroustrup in 1979, while working at AT&T Bell Laboratories 

   - • “Often referred to as C with classes” 

   - Classes are ways of creating “objects” to conduct “object-oriented” programming practices while providing low-level access and operations like C. 

   - C++ has remained mostly backwards compatible with C, and you can import C libraries directly into C++ code using #include. 

   - C++’s has since it’s creation, allowed for efficient modular programming, and it has become essential to game engine and 3D graphics programming 



<!-- Start of picture text -->
12<br><!-- End of picture text -->



<!-- Start of picture text -->
GLEW: Who, What, Where, When, Why<br><!-- End of picture text -->



- Who: Created by Milan Ikits and Marcelo Magallon, maintained currently by Nigel Stewart 

- What: Cross-platform C and C++ extension loading library. Available and tested on multiple major OS distributions (i.e. Windows and Linux). Reduces boilerplate code for accessing and utilizing GPU specific functions. Checks if a system supports certain OpenGL versions. 

- Where: Milan created while also working on his PhD thesis at Scientific Computing and Imaging Institute 

- When: Originated in 2002 

- Why: As a way to provide run-time functionality for managing supported OpenGL extensions on a target system/platform. 



<!-- Start of picture text -->
13<br><!-- End of picture text -->



<!-- Start of picture text -->
GLFW: Who, What, Where, When, Why<br><!-- End of picture text -->

- Who: Created by Marcus Geelnard. Maintained today by the GLFW Development Team 

- What: Open-source library for OpenGL and Vulkan software. It handles window management, input/output, events, and contexts and surfaces of applications. Supports major OS platforms (i.e. Windows, Linux). Programmed in C99 (C language). 

- Where: Sweden 

- When: Created in 2002 

- Why: As a way to provide simple window management for graphics applications. 



<!-- Start of picture text -->
14<br><!-- End of picture text -->



<!-- Start of picture text -->
GLM: Who, What, Where, When, Why<br><!-- End of picture text -->



- Who: Created by Christophe Riccio (French programmer) 

- What: C++ header math library for computer graphics (based on OpenGL Shading Language specs). Allows for linear algebraic operations for 3D graphics manipulation. Requires C++ 17 or newer. 

- Where: France 

- When: Created in 2005 

- Why: As a way to provide a mathematic library for 3D graphics sizing, rotating, positioning. 



<!-- Start of picture text -->
SOIL2: Who, What, Where, When, Why<br><!-- End of picture text -->





<!-- Start of picture text -->
15<br><!-- End of picture text -->

- Who: Created by Martín Lucas Golini based on Jonathan Dummer’s SOIL project. 

- What: Used for uploading textures into OpenGL. (Texturing models). Programmed in C language. 

- Where: Argentina 

- When: Created in 2017 

- Why: As a way to provide a 3D model texturing method (PNGs, JPGs, etc.) 



<!-- Start of picture text -->
16<br><!-- End of picture text -->



<!-- Start of picture text -->
Overview Context: GLEW, GLFW, GLM,<br><!-- End of picture text -->

GLEW: Handles C and C++ extensions loading for run-time OpenGL extension support determining and loads them for use 

GLFW: Handles Window management and interaction 

GLM: Handles the mathematics for 3D graphics SOIL2: Handles the image asset loading onto 3D graphics via OpenGL 



<!-- Start of picture text -->
17<br><!-- End of picture text -->



<!-- Start of picture text -->
Overview Diagram: GLEW, GLFW, GLM,<br><!-- End of picture text -->

# GLEW 

GLFW 



GLM 

SOIL2 





<!-- Start of picture text -->
18<br><!-- End of picture text -->



<!-- Start of picture text -->
Graphics Pipeline: Purpose<br><!-- End of picture text -->

- 

- 



<!-- Start of picture text -->
step<br><!-- End of picture text -->



<!-- Start of picture text -->
process that is dependent (reliant) on the<br><!-- End of picture text -->



<!-- Start of picture text -->
It takes all 3D processing instructions and runs<br><!-- End of picture text -->



<!-- Start of picture text -->
graphics<br><!-- End of picture text -->

- 



<!-- Start of picture text -->
Why: It is essential for managing a 3D graphics<br><!-- End of picture text -->

19 

Graphics Pipeline: Simplified Diagram Overview 

