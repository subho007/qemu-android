qemu-android
============

This is a direct FORK of the android emulator source, To compile this follow the instruction

###For Ubuntu based distro:

1. Install the pre-requisites 

```
sudo apt-get install git-core gnupg flex bison gperf \
build-essential zip curl zlib1g-dev libc6-dev \
libncurses5-dev x11proto-core-dev libx11-dev \
libgl1-mesa-dev g++-multilib mingw32 tofrodos \
python-markdown libxml2-utils xsltproc
```

2. Configure build.

```
./android-configure.sh --cc=/usr/bin/gcc \
--ignore-audio \
--no-gles
```

Note: This emulator build doesnot yet support opengl render, maybe fixed in future. you can run 
`./android-configure.sh -h` to get a list of available options

3. Running the installation

type in `make` to compile the source, you will get the binaries in `objs` folder

###Building in Mac OsX 10.9 (Mavericks)

Note: I have succesfully built it for Mac OsX 10.9 but the binary doesnot work since it is built by clang, alternatively
if I try to build with gcc, few parts of the source code needs clang to compile objective-C based code, Will update the code
and the readme once I figure the workaround.
