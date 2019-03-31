# $OpenBSD$
COMMENT=               simple, fast and modern VPN implemented (tools)

VERSION=               0.0.20190227

DISTNAME=              WireGuard-${VERSION}
PKGNAME=               wireguard-tools-${VERSION}

CATEGORIES=            net security
MASTER_SITES=          https://git.zx2c4.com/WireGuard/snapshot/
EXTRACT_SUFX=          .tar.xz

HOMEPAGE=              https://www.wireguard.com/

# GPLv2
PERMIT_PACKAGE_CDROM=  Yes

WANTLIB=               c

USE_GMAKE=             Yes

RUN_DEPENDS=           net/wireguard-go shells/bash

WRKBUILD=              ${WRKDIST}/src
MAKE_FLAGS=            WITH_WGQUICK=yes
FAKE_FLAGS=            DESTDIR="" MANDIR="${WRKINST}${PREFIX}/man"
ALL_TARGET=            tools
INSTALL_TARGET=        tools-install

post-extract:
	sed -i 's/install -v/install/g;s/@install/install/g' ${WRKDIST}/src/tools/Makefile

.include <bsd.port.mk>