TARGET = iphone:clang:latest:16
ARCHS = arm64

DEBUG = 0
FINALPACKAGE = 1
THEOS_PACKAGE_SCHEME = rootless

include $(THEOS)/makefiles/common.mk

TOOL_NAME = screendumpd
THEOS_PACKAGE_INSTALL_PREFIX = /var/jb

$(TOOL_NAME)_FILES = main.mm
$(TOOL_NAME)_FRAMEWORKS := IOSurface IOKit Foundation CoreFoundation CoreGraphics IOSurface
$(TOOL_NAME)_PRIVATE_FRAMEWORKS := IOMobileFramebuffer IOSurface Foundation CoreFoundation CoreGraphics IOSurface
$(TOOL_NAME)_OBJCFLAGS += -Ivncbuild/include -Iinclude
$(TOOL_NAME)_LDFLAGS += -Wl,-segalign,4000 -Lvncbuild/lib  -lvncserver -lpng -llzo2 -ljpeg -lssl -lcrypto -lz
$(TOOL_NAME)_CFLAGS = -w
$(TOOL_NAME)_CODESIGN_FLAGS = "-Sen.plist"
$(TOOL_NAME)_INSTALL_PATH = /var/jb/usr/libexec

include $(THEOS_MAKE_PATH)/tool.mk
