SUBDIRS = include . examples

AM_CPPFLAGS += \
-I$(top_srcdir)/modules/bm_sim/include \
-I$(srcdir)/include \
-I$(top_builddir)/thrift_src/gen-cpp

if P4THRIFT
  AM_CPPFLAGS += -DP4THRIFT 
endif

AM_CXXFLAGS = $(PICKY_CXXFLAGS)
AM_CFLAGS = $(PICKY_CFLAGS)

libbmapps_la_LIBADD = \
$(top_builddir)/thrift_src/libruntimestubs.la \
-lnanomsg $(THRIFT_LIB) 
libbmapps_la_LDFLAGS = -pthread

noinst_LTLIBRARIES = libbmapps.la

libbmapps_la_SOURCES = \
src/learn.cpp \
src/packet_pipe.cpp \
src/nn.h
