# Definition

Show how to use cmake for simple or big projects.

MyLib is a shared library which will generate a dll and a .lib (under Windows of course).
Main will generate a .exe and is linked (not statically) to MyLib.
`nmake install` will install the exe and the dll in the `bin` directory, and the lib in the `lib` directory.

# Generation and installation

1. Generate the build directory

`mkdir build`

2. Go inside the `build` directory

3. Generate the makefiles

`cmake -G "NMake Makefiles" ..`

4. Compile and install

`nmake install`

This command will compile and install the .dll and .exe in the `bin` directory, while the .lib will be placed in the `lib` folder.

# Using Mingw

See YouWol-Mingw on github for more info

1. Launch the msys console and use Mingw as compiler (gcc)

# Using Microsoft Visual Studio 'nmake'

1. launch cmd.exe
1. launch the ```vcvarsall.bat``` from the Visual studio installation , directory **VC** (usually in ```C:\Program Files (x86)\Microsoft Visual Studio 14.0\VC```)
2. go in the folder ```PROJECT/build``` and type ```cmake -G "NMake Makefiles" ..```
