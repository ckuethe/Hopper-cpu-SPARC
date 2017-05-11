include $(GNUSTEP_MAKEFILES)/common.make

BUNDLE_NAME = SPARCCPU
SPARCCPU_OBJC_FILES = \
	SPARCCPU/SPARCCPU.m \
	SPARCCPU/SPARCCtx.m

#NOWARN=-Wno-format -Wno-return-type -Wno-unused-value -Wno-unused-variable -Wno-self-assign
SPARCCPU_OBJCFLAGS=-I./HopperSDK/include -I./Capstone/include/ -DLINUX -fblocks -fobjc-nonfragile-abi $(NOWARN)

include $(GNUSTEP_MAKEFILES)/bundle.make
