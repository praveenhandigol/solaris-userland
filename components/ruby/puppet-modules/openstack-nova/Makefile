#
# CDDL HEADER START
#
# The contents of this file are subject to the terms of the
# Common Development and Distribution License (the "License").
# You may not use this file except in compliance with the License.
#
# You can obtain a copy of the license at usr/src/OPENSOLARIS.LICENSE
# or http://www.opensolaris.org/os/licensing.
# See the License for the specific language governing permissions
# and limitations under the License.
#
# When distributing Covered Code, include this CDDL HEADER in each
# file and include the License file at usr/src/OPENSOLARIS.LICENSE.
# If applicable, add the following below this CDDL HEADER, with the
# fields enclosed by brackets "[]" replaced with your own identifying
# information: Portions Copyright [yyyy] [name of copyright owner]
#
# CDDL HEADER END
#

#
# Copyright (c) 2015, 2017, Oracle and/or its affiliates. All rights reserved.
#

include ../../../../make-rules/shared-macros.mk

COMPONENT_NAME=		openstack-nova
COMPONENT_VERSION=      8.2.0
COMPONENT_SRC=		$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=	$(COMPONENT_SRC).tar.gz
COMPONENT_ARCHIVE_HASH= \
	sha256:362dd2597e819f16e9f23dff5779e5480554bd58c6f8511bd4fa397bd7723f82
COMPONENT_ARCHIVE_URL=	http://tarballs.openstack.org/puppet-nova/puppet-nova-$(COMPONENT_VERSION).tar.gz
COMPONENT_PROJECT_URL=	http://www.openstack.org/
COMPONENT_BUGDB=	service/nova
COMPONENT_ANITYA_ID=	13242

TPNO=			30881

include $(WS_MAKE_RULES)/prep.mk
include $(WS_MAKE_RULES)/puppetmodule.mk
# The OpenStack Puppet modules are release-specific.  Since the Mitaka
# OpenStack components are excluded from the FOSS evaluation repo,
# this module needs to be excluded as well
BUILD_BITS=NO_ARCH
include $(WS_MAKE_RULES)/no-evaluation.mk
include $(WS_MAKE_RULES)/ips.mk

MODULE_NAME =	nova

ASLR_MODE = $(ASLR_NOT_APPLICABLE)

# common targets
build:		$(BUILD_NO_ARCH)

install:	$(INSTALL_NO_ARCH)

test:		$(NO_TESTS)
