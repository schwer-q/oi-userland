#
# This file and its contents are supplied under the terms of the
# Common Development and Distribution License ("CDDL)". You may
# only use this file in accordance with the terms of the CDDL.
#
# A full copy of the text of the CDDL should have accompanied this
# source. A copy of the CDDL is also available via the Internet at
# http://www.illumos.org/license/CDDL.
#

#
# Copyright 2013 Adam Stevko. All rights reserved.
#

include ../../../make-rules/shared-macros.mk

COMPONENT_NAME=   libstatgrab
COMPONENT_VERSION=  0.91
COMPONENT_FMRI= library/$(COMPONENT_NAME)
COMPONENT_CLASSIFICATION= Development/C
COMPONENT_PROJECT_URL=  http://www.i-scream.org/$(COMPONENT_NAME)
COMPONENT_SRC= $(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE= $(COMPONENT_SRC).tar.gz
COMPONENT_ARCHIVE_HASH= sha256:03e9328e4857c2c9dcc1b0347724ae4cd741a72ee11acc991784e8ef45b7f1ab
COMPONENT_ARCHIVE_URL=  http://dl.ambiweb.de/mirrors/ftp.i-scream.org/$(COMPONENT_NAME)/$(COMPONENT_ARCHIVE)
COMPONENT_LICENSE= GPLv2	
COMPONENT_SUMMARY= libstatgrab is a library that provides cross platform access to statistics about the system on which it's run.


include $(WS_MAKE_RULES)/prep.mk
include $(WS_MAKE_RULES)/configure.mk
include $(WS_MAKE_RULES)/ips.mk

PATCH_LEVEL= 1

COMPONENT_PRE_CONFIGURE_ACTION=($(CLONEY) $(SOURCE_DIR) $(@D))


build:          $(BUILD_32)

install:        $(INSTALL_32)

test:           $(TESTS_32)

REQUIRED_PACKAGES += library/ncurses
REQUIRED_PACKAGES += system/library
