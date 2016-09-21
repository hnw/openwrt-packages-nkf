include $(TOPDIR)/rules.mk

PKG_NAME:=nkf
PKG_VERSION:=2.1.4
PKG_RELEASE:=1

PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE:=$(PKG_SOURCE_SUBDIR).tar.gz
PKG_SOURCE_URL:=http://dl.osdn.jp/nkf/64158/
PKG_MD5SUM:=dbce0a2131cd4e30f73cbfdcc57c06ec

PKG_BUILD_PARALLEL:=1
PKG_INSTALL:=1
PKG_USE_MIPS16:=0

PKG_LICENSE:=MIT
PKG_MAINTAINER:=Yoshio HANAWA <for-openwrt@hnw.jp>

include $(INCLUDE_DIR)/package.mk

define Package/nkf
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=Network Kanji code conversion Filter (NKF)
  URL:=https://osdn.jp/projects/nkf/
endef

define Package/nkf/description
  Network Kanji code conversion Filter (NKF)
endef

MAKE_INSTALL_FLAGS += \
  prefix="$(PKG_INSTALL_DIR)" \
  MKDIR="mkdir -p"

define Package/nkf/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/bin/nkf $(1)/usr/bin/
endef

$(eval $(call BuildPackage,nkf))
