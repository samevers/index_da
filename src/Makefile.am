include $(top_srcdir)/common.mk

bin_PROGRAMS=
lib_LIBRARIES=
lib_LTLIBRARIES=
SUBDIRS=

lib_LTLIBRARIES+=libindex_da.la
libindex_da_la_SOURCES=Index_da.cpp GraphSegmentor.cpp WordSegmentor.cpp
libindex_da_la_LIBADD=-lpthread -lssplatform -lencoding -lgflags -lglog -lgtest -lIQSegmentor -ldicmap  -lCoreSegmentor
AM_CPPFLAGS=-DSS_DOCID_BITS=256 -I./
libindex_da_la_CPPFLAGS=$(AM_CPPFLAGS) -DSS_DOCID_BITS=256


##
bin_PROGRAMS=make_index
make_index_SOURCES=main.cpp
make_index_LDADD= -lssplatform -lencoding -lindex_da -ldicmap
make_index_LDFLAGS=-DHAVE_CXX_STDHEADERS -DLINUX -DACE_HAS_EVENT_POLL -D_FILE_OFFSET_BITS=64 -fPIC -ggdb

AM_CPPFLAGS=-DSS_DOCID_BITS=256 -I./


#AM_CPPFLAGS+=-I../sys

