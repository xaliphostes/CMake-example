# Definition
MyLib is a shared library which will generate a dll and a .lib (under Windows of course).
Main will generate a .exe and is linked (not statically) to MyLib.
`nmake install` will install the exe and the dll in the `bin` directory, and the lib in the `lib` directory.

1. Generate the build directory

2. Go inside

3. Generate the makefiles
`cmake -G "NMake Makefiles" ..`

4. Compile
`nmake`

5. Install
`nmake install`
Installation will be done in the `bin` directory.
