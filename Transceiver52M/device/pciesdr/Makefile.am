include $(top_srcdir)/Makefile.common

PCIESDR_DIR = $(PCIESDR_LIB)

AM_CPPFLAGS = -Wall $(STD_DEFINES_AND_INCLUDES) -I${srcdir}/../common -I${PCIESDR_DIR}/kernel -I${PCIESDR_DIR}/api

AM_CXXFLAGS = $(LIBOSMOCORE_CFLAGS) $(LIBOSMOCTRL_CFLAGS) $(LIBOSMOVTY_CFLAGS)

LDADD = -lpthread -lsdr $(LIBOSMOCORE_LIBS) $(LIBOSMOCTRL_LIBS) $(LIBOSMOVTY_LIBS)

noinst_HEADERS = PCIESDRDevice.h

noinst_LTLIBRARIES = libdevice.la

libdevice_la_SOURCES = PCIESDRDevice.cpp
libdevice_la_LIBADD = $(top_builddir)/Transceiver52M/device/common/libdevice_common.la
