#
# Copyright (C) 2010-2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=perl-www-mechanize
PKG_VERSION:=1.74
PKG_RELEASE:=2

PKG_SOURCE:=WWW-Mechanize-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=http://www.cpan.org/authors/id/E/ET/ETHER/
PKG_MD5SUM:=8ec615225037ac66a2d37f4e9693ef86

PKG_LICENSE:=GPL-1.0+ Artistic-1.0-Perl
PKG_MAINTAINER:=Marcel Denia <naoir@gmx.net>

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/WWW-Mechanize-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include ../perl/perlmod.mk

define Package/perl-www-mechanize
  SUBMENU:=Perl
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=Perl WWW Mechanize
  URL:=http://search.cpan.org/dist/WWW-Mechanize/
  DEPENDS:=perl +perl-www
endef

define Build/Configure
	$(call perlmod/Configure,$(STAGING_DIR)/usr/include,)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-www-mechanize/install
	$(call perlmod/Install,$(1),WWW/Mechanize WWW/Mechanize.pm)
endef


$(eval $(call BuildPackage,perl-www-mechanize))
