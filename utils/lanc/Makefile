include $(TOPDIR)/rules.mk

PKG_NAME:=lanc
PKG_VERSION:=0.1.0
PKG_RELEASE=1
PKG_LICENSE:=MIT
PKG_GOGET:=github.com/Akagi201/lancaster/cmd/lanc

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/golang.mk

define Package/lanc
  SECTION:=base
  CATEGORY:=Base system
  TITLE:=Lancaster client
endef

define Package/lanc/description
   Lancaster client
endef

define Build/Compile
	( \
		cd $(PKG_BUILD_DIR); \
		mkdir -p bin; \
		cd src/$(PKG_GOGET); \
		PATH="$(GOROOT)/bin:$$$$PATH" \
		GOPATH=$(PKG_BUILD_DIR) GOOS=linux GOARCH=$(GOARCH) go build; \
	)
endef

define Package/lanc/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/src/github.com/Akagi201/cmd/$(PKG_NAME) $(1)/usr/bin
endef

$(eval $(call BuildPackage,lanc))