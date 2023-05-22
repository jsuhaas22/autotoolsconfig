#CROSS_COMPILE ?= aarch64-linux-gnu-
#CC = $(CROSS_COMPIILE)gcc
DEF_INC = $(shell $(CC)  -print-file-name=include)
DEF_INC_PATH = -I. -Iinclude
#STATIC_BUILD ?= -static

MYCFLAGS = $(CFLAGS) -Wall -Wextra -Wno-missing-field-initializers -I$(DEF_INC) $(DEF_INC_PATH)

#ifdef DEBUG
#MYCFLAGS+=-g3 -fno-inline -O0 -DDEBUG
#else
#MYCFLAGS+=-0s
#endif

AM_CC = $(CC)
AM_CFLAGS = $(MYCFLAGS)

#SOURCEDIRS = common soc/am62ax soc/am62x soc/am64x soc/am65x soc/am65x_sr2
#soc/j7200 soc/j721e soc/j721s2 soc/j784s4

#bin_PROGRAMS = k3conf
#k3conf_SOURCES = $(foreach dir,$(SOURCESDIRS),$(wildcard $(dir)/*.c)) 
#nobase_include_HEADERS = $(foreach dir,$(SOURCEDIRS),$(wildcard $(dir)/*.h))

AUTOMAKE_OPTIONS = subdir-objects

COMMONSOURCES=\
		common/k3conf.c \
		common/help.c \
		common/mmio.c \
		common/socinfo.c \
		common/sec_proxy.c \
		common/tisci/tisci_core.c \
		common/tisci/tisci_device.c \
		common/tisci/tisci_clock.c \
		common/autoadjust_table.c \
		common/cmd_show.c \
		common/cmd_dump.c \
		common/cmd_enable.c \
		common/cmd_disable.c \
		common/cmd_set.c \
		common/cmd_rw.c

COMMONHEADERS=$(COMMONSOURCES:.c=.o)

AM65XSOURCES =\
	      soc/am65x/am65x_host_info.c \
	      soc/am65x/am65x_sec_proxy_info.c \
	      soc/am65x/am65x_processors_info.c \
	      soc/am65x/am65x_devices_info.c \
	      soc/am65x/am65x_clocks_info.c \
	      soc/am65x/am65x_rm_info.c \
	      soc/am65x_sr2/am65x_sr2_host_info.c \
	      soc/am65x_sr2/am65x_sr2_sec_proxy_info.c \
	      soc/am65x_sr2/am65x_sr2_processors_info.c \
	      soc/am65x_sr2/am65x_sr2_devices_info.c \
	      soc/am65x_sr2/am65x_sr2_clocks_info.c \
	      soc/am65x_sr2/am65x_sr2_rm_info.c

AM65XHEADERS=$(AM65XSOURCES:.c=.o)

J721ESOURCES =\
	      soc/j721e/j721e_host_info.c \
	      soc/j721e/j721e_sec_proxy_info.c \
	      soc/j721e/j721e_processors_info.c \
	      soc/j721e/j721e_devices_info.c \
	      soc/j721e/j721e_clocks_info.c \
	      soc/j721e/j721e_rm_info.c \
	      soc/j7200/j7200_host_info.c \
	      soc/j7200/j7200_sec_proxy_info.c \
	      soc/j7200/j7200_processors_info.c \
	      soc/j7200/j7200_devices_info.c \
	      soc/j7200/j7200_clocks_info.c \
	      soc/j7200/j7200_rm_info.c

J721EHEADERS=$(J721ESOURCES:.c=.o)

AM64XSOURCES =\
	      soc/am64x/am64x_host_info.c \
	      soc/am64x/am64x_sec_proxy_info.c \
	      soc/am64x/am64x_processors_info.c \
	      soc/am64x/am64x_devices_info.c \
	      soc/am64x/am64x_clocks_info.c \
	      soc/am64x/am64x_rm_info.c

AM64XHEADERS=$(AM64XSOURCES:.c=.o)

AM62XSOURCES =\
	      soc/am62x/am62x_devices_info.c \
	      soc/am62x/am62x_clocks_info.c \
	      soc/am62x/am62x_host_info.c \
	      soc/am62x/am62x_processors_info.c \
	      soc/am62x/am62x_rm_info.c \
	      soc/am62x/am62x_sec_proxy_info.c

AM62XHEADERS=$(AM62XSOURCES:.c=.o)

J721S2SOURCES =\
	      soc/j721s2/j721s2_devices_info.c \
	      soc/j721s2/j721s2_clocks_info.c \
	      soc/j721s2/j721s2_host_info.c \
	      soc/j721s2/j721s2_processors_info.c \
	      soc/j721s2/j721s2_rm_info.c \
	      soc/j721s2/j721s2_sec_proxy_info.c

J721S2HEADERS=$(J721S2SOURCES:.c=.o)

J784S4SOURCES =\
	      soc/j784s4/j784s4_clocks_info.c \
	      soc/j784s4/j784s4_devices_info.c \
	      soc/j784s4/j784s4_host_info.c \
	      soc/j784s4/j784s4_processors_info.c \
	      soc/j784s4/j784s4_rm_info.c \
	      soc/j784s4/j784s4_sec_proxy_info.c

J784S4HEADERS=$(J784S4SOURCES:.c=.o)

AM62AXSOURCES =\
	      soc/am62ax/am62ax_clocks_info.c \
	      soc/am62ax/am62ax_devices_info.c \
	      soc/am62ax/am62ax_host_info.c \
	      soc/am62ax/am62ax_processors_info.c \
	      soc/am62ax/am62ax_rm_info.c \
	      soc/am62ax/am62ax_sec_proxy_info.c

AM62AXHEADERS=$(AM62AXSOURCES:.c=.o)

COMMONOBJECTS=	$(COMMONSOURCES:.c=.o)
AM65XOBJECTS=	$(AM65XSOURCES:.c=.o)
J721EOBJECTS=	$(J721ESOURCES:.c=.o)
AM64XOBJECTS=	$(AM64XSOURCES:.c=.o)
AM62XOBJECTS=	$(AM62XSOURCES:.c=.o)
J721S2OBJECTS=  $(J721S2SOURCES:.c=.o)
J784S4OBJECTS=	$(J784S4SOURCES:.c=.o)
AM62AXOBJECTS=	$(AM62AXSOURCES:.c=.o)

ALLOBJECTS=	$(COMMONOBJECTS) $(AM65XOBJECTS) $(J721EOBJECTS) \
		$(AM64XOBJECTS) $(AM62XOBJECTS) $(J721S2OBJECTS) \
		$(J784S4OBJECTS) $(AM62AXOBJECTS)

INCLUDEHEADERS = include/autoadjust_table.h include/help.h include/k3conf.h \
include/mmio.h include/sec_proxy.h include/socinfo.h include/tisci.h \
include/tisci_protocol.h include/version.h

k3confdir = $(includedir)/k3conf

bin_PROGRAMS = k3conf
k3conf_SOURCES = $(COMMONSOURCES) $(AM62XSOURCES) $(AM62AXSOURCES) \ 
$(AM64XSOURCES) $(AM65XSOURCES) $(J721S2SOURCES) $(J784S4SOURCES) \ 
$(J721ESOURCES) builddate.c version.c
k3conf_HEADERS = $(INCLUDEHEADERS)
nobase_include_HEADERS = $(COMMONHEADERS) $(AM62XHEADERS) $(AM62AXHEADERS) \ 
$(AM64XHEADERS) $(AM65XHEADERS) $(J721S2HEADERS) $(J784S4HEADERS) \ 
$(J721EHEADERS) $(INCLUDEHEADERS)

DIST_EXTRA = $(man_MANS) README COPYING

builddate.c:	$(ALLOBJECTS)
		@echo 'char *builddate="'`date`'";' > builddate.c

version.c:	$(ALLOBJECTS)
		@echo 'char *k3conf_version="'`git describe --dirty 2>/dev/null||echo "$(VERSION_MAJOR).$(VERSION_MINOR)-nogit"`'";' > version.c
