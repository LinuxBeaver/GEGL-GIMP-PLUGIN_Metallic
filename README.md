Download binaries here.
https://github.com/LinuxBeaver/gimp-metallic-plugin-Make-people-metal-with-GEGL/releases

GEGL Metallic
=========

![image](https://github.com/LinuxBeaver/gegl-metallic---Make-people-metal-with-GEGL/assets/78667207/b71f8ead-fae2-4016-84aa-10bd33596d0e)


![image](https://github.com/LinuxBeaver/gegl-metallic---Make-people-metal-with-GEGL/assets/78667207/25cfe85a-7c3a-4136-bc49-64c09dcd5c68)


A custom GEGL operation (and by extension GIMP filter) that makes people metal


## OS specific location to put GEGL Filter binaries 

Windows
 C:\\Users\<YOUR NAME>\AppData\Local\gegl-0.4\plug-ins
 
 Linux 
 /home/(USERNAME)/.local/share/gegl-0.4/plug-ins
 
 Linux (Flatpak)
 /home/(USERNAME)/.var/app/org.gimp.GIMP/data/gegl-0.4/plug-ins



## Compiling and Installing

### Linux

To compile and install you will need the GEGL header files (`libgegl-dev` on
Debian based distributions or `gegl` on Arch Linux) and meson (`meson` on
most distributions).

```bash
meson setup --buildtype=release build
ninja -C build
cp build/high-pass-box.so ~/.local/share/gegl-0.4/plug-ins
```

If you have an older version of gegl you may need to copy to `~/.local/share/gegl-0.3/plug-ins`
instead (on Ubuntu 18.04 for example).



### Windows

The easiest way to compile this project on Windows is by using msys2.  Download
and install it from here: https://www.msys2.org/

Open a msys2 terminal with `C:\msys64\mingw64.exe`.  Run the following to
install required build dependencies:

```bash
pacman --noconfirm -S base-devel mingw-w64-x86_64-toolchain mingw-w64-x86_64-meson mingw-w64-x86_64-gegl
```

Then build the same way you would on Linux:

```bash
meson setup --buildtype=release build
ninja -C build
```

More previews of this based plugin turning things gold

![image](https://github.com/LinuxBeaver/gegl-metallic---Make-people-metal-with-GEGL/assets/78667207/247e4d8e-5b6f-4b17-a8f5-561470be0bf7)


![image](https://github.com/LinuxBeaver/gegl-metallic---Make-people-metal-with-GEGL/assets/78667207/8519297a-26cf-4d1e-a6da-b71429bd2628)
