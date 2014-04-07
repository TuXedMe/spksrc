

PKG_NAME = ruby21
PKG_VERS = 2.1.1/ruby-2.1.1.tar.gz
PKG_EXT = tar.gz
PKG_DIST_NAME = ruby-$(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = http://cache.ruby-lang.org/pub/ruby/2.1
PKG_DIR = ruby-$(PKG_VERS)

DEPENDS  = cross/zlib cross/openssl cross/sqlite cross/readline cross/ncurses cross/bzip2

MAINTAINER = tuxedme@gmail.com
HOMEPAGE   = http://www.ruby-lang.org
COMMENT    = Ruby Programming Language
LICENSE    =

# Patch
#POST_PATCH_TARGET = pyPostPatch

# Configure
GNU_CONFIGURE = 1
#ADDITIONAL_CFLAGS =  -D_LARGEFILE64_SOURCE -D_FILE_OFFSET_BITS=64
#CONFIGURE_ARGS = --enable-ipv6 ac_cv_buggy_getaddrinfo=no

# Compile
#COMPILE_TARGET = myCompile

# Install
#INSTALL_TARGET = myInstall
#POST_INSTALL_TARGET = $(WORK_DIR)/python-cc.mk

include ../../mk/spksrc.cross-cc.mk

#HOSTPYTHON_NATIVE = $(WORK_DIR)/../../../native/$(PKG_NAME)/work-native/$(PKG_DIR)/python
#HOSTPYTHON_LIB_NATIVE = $(WORK_DIR)/../../../native/$(PKG_NAME)/work-native/$(PKG_DIR)/build/lib.linux-i686-2.7
#PYTHON_LIB_CROSS = $(WORK_DIR)/$(PKG_DIR)/build/lib.linux-i686-2.7
#HOSTPGEN_NATIVE = $(WORK_DIR)/../../../native/$(PKG_NAME)/work-native/$(PKG_DIR)/Parser/pgen
#PYTHON_LIB_DIR = lib/python2.7

#HOSTPYTHON = $(WORK_DIR)/$(PKG_DIR)/hostpython
#HOSTPGEN = $(WORK_DIR)/$(PKG_DIR)/hostpgen

#pyPostPatch:
#	$(RUN) sed -e 's#@INSTALL_PREFIX@#$(INSTALL_PREFIX)#' -i Lib/mimetypes.py

#myCompile:
#	cp $(HOSTPYTHON_NATIVE) $(HOSTPYTHON)
#	cp $(HOSTPGEN_NATIVE) $(HOSTPGEN)
#	$(RUN) $(MAKE) HOSTPYTHON=$(HOSTPYTHON) HOSTPGEN=$(HOSTPGEN) CROSS_COMPILE_TARGET=yes
	
#myInstall:
#	@install -m 755 -d $(STAGING_INSTALL_PREFIX)/etc
#	@install -m 644 src/mime.types $(STAGING_INSTALL_PREFIX)/etc/
#	$(RUN) $(MAKE) HOSTPYTHON=$(HOSTPYTHON) HOSTPGEN=$(HOSTPGEN) CROSS_COMPILE_TARGET=yes install prefix=$(STAGING_INSTALL_PREFIX)

#$(WORK_DIR)/python-cc.mk: Makefile
#	@echo HOSTPYTHON=$(HOSTPYTHON) > $@
#	@echo HOSTPYTHON_LIB_NATIVE=$(HOSTPYTHON_LIB_NATIVE) >> $@
#	@echo PYTHON_LIB_CROSS=$(PYTHON_LIB_CROSS) >> $@
#	@echo PYTHON_LIB_DIR=$(PYTHON_LIB_DIR) >> $@
