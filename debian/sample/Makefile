#!/usr/bin/make -f

export DEB_BUILD_MAINT_OPTIONS = hardening=+all
DPKG_EXPORT_BUILDFLAGS = 1
include /usr/share/dpkg/default.mk

INCDIR1=$(T)/../include
INCDIR2=$(T)/include
LIBDIR=$(T)/lib/.libs

CPPFLAGS += -DPLUGINDIR=\"/usr/lib/$(DEB_HOST_MULTIARCH)/sasl2\"
CPPFLAGS += -I. -I$(T) -I$(INCDIR1) -I$(INCDIR2) -L$(LIBDIR)
LDLIBS = -lsasl2

all: sample/sample-server sample/sample-client
