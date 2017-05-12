include $(GNUSTEP_MAKEFILES)/common.make

BUNDLE_NAME = SPARCCPU
SPARCCPU_OBJC_FILES = \
	SPARCCPU/SPARCCPU.m \
	SPARCCPU/SPARCCtx.m

#NOWARN=-Wno-format -Wno-return-type -Wno-unused-value -Wno-unused-variable -Wno-self-assign
SPARCCPU_OBJCFLAGS=$(NOWARN) \
	-I${HOME}/GNUstep/Library/ApplicationSupport/Hopper/HopperSDK/include \
	-I./Capstone/include/ \
	-DLINUX

include $(GNUSTEP_MAKEFILES)/bundle.make
