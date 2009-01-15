
METASOURCES = AUTO

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = libtinydict.pc

if WITH_JINKE
noinst_LTLIBRARIES = libtinydict.la
else
lib_LTLIBRARIES = libtinydict.la
endif

include_HEADERS = tinydict.h
libtinydict_la_LDFLAGS = -no-undefined -version-info 0:0:0
libtinydict_la_SOURCES = tinydict.cpp

AM_CXXFLAGS = -Wall
AM_CFLAGS = 
