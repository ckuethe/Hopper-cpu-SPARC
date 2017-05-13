# Hopper SPARC plugin
SPARC CPU plugin for the Hopper Disassembler, inspired by plugins for
[ST20](https://github.com/bSr43/HopperST20C2C4-plugin),
[M68k](https://github.com/0xc010d/HopperSDK/tree/master/Samples/M68kCPU), and
[MIPS](https://github.com/makigumo/MIPSCPU) CPUs.

This plugin was developed on Ubuntu, and uses a Makefile to build;
XCode support is untested.

# Build Instructions

Install either the [Hopper SDK](https://github.com/0xc010d/HopperSDK)
or the [Linux SDK](https://github.com/ckuethe/HopperSDK-Linux)

```
. ${HOME}/hopper-gnustep.sh
git clone https://github.com/ckuethe/Hopper-cpu-SPARC
cd Hopper-cpu-SPARC
# check settings in Makefile for sanity
make
DEST=${HOME}/GNUstep/Library/ApplicationSupport/Hopper/PlugIns/v4/CPUs/
mkdir -p $DEST
ln -s ${PWD}/SPARCCPU.bundle ${DEST}/SPARC.hopperCPU
```
