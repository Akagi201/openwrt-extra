include $(TOPDIR)/rules.mk

PKG_NAME:=hellocmake
PKG_VERSION:=0.1.0
PKG_RELEASE=1
PKG_LICENSE:=MIT

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/hellocmake
  SECTION:=base
  CATEGORY:=Base system
  TITLE:=hellocmake title (TEST)
endef

define Package/hellocmake/description
   hellocmake description (TEST)
endef

define Package/hellocmake/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/hellocmake $(1)/usr/bin/
endef

$(eval $(call BuildPackage,hellocmake))