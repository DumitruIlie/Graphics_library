# Graphics.h library

This is not my code, it is just a place where I store the libraries so anyone can download and install them. The library instalation process is detailed and short, however it is only written for Codeblocks 16.01. For other versions/compilers the installation process is similar.

## Instalation process

In the original `/MinGW/include/graphics.h` file, at line $302$ there was an error regarding a name. That I have fixed but I leave this as a helper for anyone seeking the fix. If you get an error then try replacing line $302$ with
```C++
int left=0, int top=0, int right=INT_MAX, int bottom=INT_MAX,
```

1. Copy the `graphics.h` and `windows.h` files from `/MinGW/include/` to the `include` directory of your compiler. To find it for codeblocks open the file location of the codeblocks executable, then go to `/MinGW/include/`.
2. Copy the `libbgi.a` file from `/MinGW/lib/` to the `lib` directory of your compiler. To find it for codeblocks open the file location of the codeblocks executable, then go to `/MinGW/lib/`.
3. Open Codeblocks.
4. Go to `Settings`>`Compiler...`>`Global compiler settings`>`Linker settings`
5. Paste the following line in `Other linker options:`: `-lbgi -lgdi32 -lcomdlg32 -luuid -loleaut32 -lole32`
6. You are done.

There is an example file to check if there are any errors, it is `clock.cpp` (**Note: M_PI might not be defined**. To fix just define the variable or change the C++ standard version). I also attached an example of window drawn (`clock_expected_output_example.png`).

To test you can also use any of my other projects built with the library.

### info.txt

The file came from my profesor together with everything. I keep it here in case I (or someone else) needs it.