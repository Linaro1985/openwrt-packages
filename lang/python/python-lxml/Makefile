#
# Copyright (C) 2017 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python-lxml
PKG_VERSION:=5.2.1
PKG_RELEASE:=1

PYPI_NAME:=lxml
PKG_HASH:=3f7765e69bbce0906a7c74d5fe46d2c7a7596147318dbc08e4a2431f3060e306

PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=LICENSES.txt
PKG_MAINTAINER:=Alexandru Ardelean <ardeleanalex@gmail.com>
PKG_CPE_ID:=cpe:/a:lxml:lxml

PKG_BUILD_DEPENDS:=python-cython/host

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-lxml
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Pythonic XML processing library
  URL:=https://lxml.de
  DEPENDS:=+libxml2 +libxslt +libexslt +python3-light
endef

define Package/python3-lxml/description
  lxml is a Pythonic, mature binding for the libxml2 and libxslt
  libraries. It provides safe and convenient access to these libraries
  using the ElementTree API.

  It extends the ElementTree API significantly to offer support for
  XPath, RelaxNG, XML Schema, XSLT, C14N and much more.
endef

$(eval $(call Py3Package,python3-lxml))
$(eval $(call BuildPackage,python3-lxml))
$(eval $(call BuildPackage,python3-lxml-src))
