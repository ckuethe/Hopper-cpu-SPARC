# Hopper SPARC plugin
SPARC CPU plugin for the Hopper Disassembler, inspired by plugins for
[ST20](https://github.com/bSr43/HopperST20C2C4-plugin),
[M68k](https://github.com/0xc010d/HopperSDK/tree/master/Samples/M68kCPU), and
[MIPS](https://github.com/makigumo/MIPSCPU) CPUs.

This plugin was developed on Ubuntu, and uses a Makefile to build;
XCode support is untested.

# Build Instructions

Clang is required to build Hopper plugins, because the
[Hopper SDK](https://github.com/0xc010d/HopperSDK) uses Blocks,
which can't be compiled by gcc. The
[Linux SDK](https://www.hopperapp.com/blog/?p=150) page indicates
that other packages will also need to be patched and built.

```
apt install clang libblocksruntime-devel libkqueue-dev libpthread-workqueue-dev
```

Blocks also require runtime support from the likes of libobjc2. While it is possible to directly install libobjc from source, packaging is done here for ease of system adminstration (ie. upgrades and uninstalls).

```
git clone https://github.com/gnustep/libobjc2
mkdir libobjc2/build
cd libobjc2/build
cmake -DCMAKE_CXX_COMPILER=clang -DCMAKE_C_COMPILER=clang -DCMAKE_ASM_COMPILER=clang -DCMAKE_ASM_FLAGS=-c -DTESTS=OFF -DCPACK_GENERATOR=DEB -DCMAKE_BUILD_TYPE=Release ..
make -j4
make package
sudo dpkg -i ./libobjc-*-Linux.deb
cd ../..
```

More instructions to follow...
