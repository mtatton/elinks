top_builddir=../..
include $(top_builddir)/Makefile.config
INCLUDES += $(SPIDERMONKEY_CFLAGS)

SUBDIRS-$(CONFIG_ECMASCRIPT_SMJS)	+= spidermonkey

OBJS-$(CONFIG_ECMASCRIPT_SMJS)		+= ecmascript.o spidermonkey.o

ifeq ($(CONFIG_ECMASCRIPT_SMJS), yes)
CONFIG_ANY_SPIDERMONKEY = yes
else ifeq ($(CONFIG_SCRIPTING_SPIDERMONKEY), yes)
CONFIG_ANY_SPIDERMONKEY = yes
else
CONFIG_ANY_SPIDERMONKEY = no
endif

OBJS-$(CONFIG_ANY_SPIDERMONKEY) += spidermonkey-shared.o

include $(top_srcdir)/Makefile.lib
