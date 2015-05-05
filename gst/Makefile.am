#
# Makefile.am for the Nice Glib ICE library
#
# (C) 2006, 2007 Collabora Ltd.
# (C) 2006, 2007 Nokia Corporation. All rights reserved.
#
# Licensed under MPL 1.1/LGPL 2.1. See file COPYING.

AM_CFLAGS = $(LIBNICE_CFLAGS) \
	-I $(top_srcdir) \
	-I $(top_srcdir)/socket \
	-I $(top_srcdir)/agent \
	-I $(top_srcdir)/random \
	-I $(top_srcdir)/stun

COMMON_LIBADD = \
	$(top_builddir)/nice/libkmsnice.la

# libgstkmsnice

if WITH_GSTREAMER
gstplugin_LTLIBRARIES = libgstkmsnice.la

libgstkmsnice_la_CFLAGS = $(AM_CFLAGS) $(GST_CFLAGS) -DGST_USE_UNSTABLE_API

libgstkmsnice_la_SOURCES = \
	gstnicesrc.h \
	gstnicesrc.c \
	gstnicesink.h \
	gstnicesink.c \
	gstnice.h \
	gstnice.c

libgstkmsnice_la_LIBADD = 	$(COMMON_LIBADD) $(GST_LIBS)

libgstkmsnice_la_LDFLAGS = -module -avoid-version -no-undefined
endif

if WITH_GSTREAMER105
gstplugin105_LTLIBRARIES = libgstkmsnice105.la

libgstkmsnice105_la_CFLAGS = $(AM_CFLAGS) $(GST_CFLAGS) -DGST_USE_UNSTABLE_API

libgstkmsnice105_la_SOURCES = \
	gstnicesrc.h \
	gstnicesrc.c \
	gstnicesink.h \
	gstnicesink.c \
	gstnice.h \
	gstnice.c

libgstkmsnice105_la_LIBADD = 	$(COMMON_LIBADD) $(GST_LIBS)

libgstkmsnice105_la_LDFLAGS = -module -avoid-version -no-undefined
endif

if WITH_GSTREAMER010
gstplugin010_LTLIBRARIES = libgstkmsnice010.la

libgstkmsnice010_la_CFLAGS = $(AM_CFLAGS) $(GST010_CFLAGS)

libgstkmsnice010_la_SOURCES = \
	gstnicesrc.h \
	gstnicesrc.c \
	gstnicesink.h \
	gstnicesink.c \
	gstnice.h \
	gstnice.c

libgstkmsnice010_la_LIBADD = $(COMMON_LIBADD) $(GST010_LIBS)

libgstkmsnice010_la_LDFLAGS = -module -avoid-version -no-undefined
endif
