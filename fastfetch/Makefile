include $(TOPDIR)/rules.mk

PKG_NAME:=fastfetch
PKG_VERSION:=2.17.1
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/fastfetch-cli/fastfetch.git
PKG_SOURCE_VERSION:=b001ea409b93ff8e5d5d660a5f5bc786cda170f7
PKG_MIRROR_HASH:=0d966b04b23ed41256be101cfa9eab2a55cf0d7ff7c40d4cd3328de2e8c63199

PKG_BUILD_DIR:=$(BUILD_DIR)/fastfetch-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/fastfetch
	CATEGORY:=Utilities
	TITLE:=Like neofetch, but much faster because written mostly in C.
endef

define Package/fastfetch/description
	Fastfetch is a neofetch-like tool for fetching system information and displaying them in a pretty way.
endef

define Package/fastfetch/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/fastfetch $(1)/usr/bin/
endef

$(eval $(call BuildPackage,fastfetch))
