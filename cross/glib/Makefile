PKG_NAME = glib
PKG_SHORT_VERS = 2.57
PKG_VERS = $(PKG_SHORT_VERS).1
PKG_EXT = tar.xz
PKG_DIR = $(PKG_NAME)-$(PKG_VERS)
PKG_DIST_NAME = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = http://ftp.gnome.org/pub/GNOME/sources/$(PKG_NAME)/$(PKG_SHORT_VERS)

DEPENDS = native/glib cross/libffi cross/pcre cross/zlib

HOMEPAGE = http://developer.gnome.org/glib/
COMMENT  = General-purpose utility library
LICENSE  = GPLv2

GNU_CONFIGURE = 1
CONFIGURE_ARGS = --disable-modular-tests --disable-gtk-doc-html --disable-man --disable-libmount
CONFIGURE_ARGS += glib_cv_long_long_format=ll glib_cv_stack_grows=no glib_cv_uscore=no ac_cv_func_posix_getpwuid_r=yes ac_cv_func_posix_getgrgid_r=yes
CONFIGURE_ARGS += GLIB_GENMARSHAL=$(WORK_DIR)/../../../native/glib/work-native/$(PKG_DIR)/gobject/glib-genmarshal
CONFIGURE_ARGS += GLIB_COMPILE_SCHEMAS=$(WORK_DIR)/../../../native/glib/work-native/$(PKG_DIR)/gio/glib-compile-schemas
CONFIGURE_ARGS += GLIB_COMPILE_RESOURCES=$(WORK_DIR)/../../../native/glib/work-native/$(PKG_DIR)/gio/glib-compile-resources

include ../../mk/spksrc.cross-cc.mk
