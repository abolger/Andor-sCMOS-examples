# Andor-sCMOS-examples
Andor sCMOS (Neo and Zyla) SDK3 examples focused on simplicity and speed.

## Prereqs
You don't have to install Cmake and Make, but they do make compiling easier.

### Windows
step 4 is necessary because not all compilers understand how to link the `.dll` files directly; the `.lib` act as a shim to the `.dll`.

1. clone this repository
2. [install Andor SDK3 for Windows](https://www.scivision.co/andor-neo-windows-sdk3-install/)
3. copy from `c:/Program Files/Andor SDK3/` directory into `andor-scmos-examples/lib/` the files

    atcorem.lib
    atcore.dll
    atutilitym.lib
    atutility.dll
4. in `andor-scmos-examples/lib`

        rename atcorem.lib atcore.lib
        rename atutilitym.lib atutility.lib
5. (optional) install [Cmake](https://cmake.org/download/) (the `.msi` file)
6. (optional) install [Make](https://sourceforge.net/projects/mingw/) all you need is under All Packages > `mingw32-make`

### Linux
I use Andor cameras with Ubuntu 16.04. 
Other Linux versions would likely work as well.

1. clone this repository
2. [install Andor SDK3 for Linux](https://www.scivision.co/andor-neo-linux-sdk3-install/)
3. install Cmake & Make

        sudo apt install cmake make g++

## Compile Andor sCMOS example programs

from the `andor-cmos-examples` directory

    cmake .
    make

this creates executable in the same top-level directory.
If you don't have a camera, the SimCam will be used.
