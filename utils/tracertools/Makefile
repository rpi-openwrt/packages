#
# Copyright (C) 2007-2014 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=tracertools
PKG_VERSION:=20141022
PKG_RELEASE=$(PKG_SOURCE_VERSION)
PKG_MAINTAINER:=Daniel Golle <daniel@makrotopia.org>

PKG_LICENSE:=GPL-3.0

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://gitorious.org/tracertools/tracertools.git
PKG_SOURCE_VERSION:=9c3c2e8b81fb8745752ee195b028a50b88dc711b
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz

PKG_INSTALL:=1

include $(INCLUDE_DIR)/package.mk

define Package/tracertools
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=Tracer MPPT monitoring and control tools
endef

define Package/tracertools/description
	Tools for the Tracer MPPT solar charge controller.
endef

define Package/tracertools/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/tracerstat $(1)/usr/bin/
endef

$(eval $(call BuildPackage,tracertools))
