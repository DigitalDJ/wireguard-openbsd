# $OpenBSD$
COMMENT=               fast, modern, secure VPN tunnel (tools)

VERSION=               0.0.20190702

DISTNAME=              WireGuard-${VERSION}
PKGNAME=               wireguard-tools-${VERSION}

CATEGORIES=            net security
MASTER_SITES=          https://git.zx2c4.com/WireGuard/snapshot/
EXTRACT_SUFX=          .tar.xz

HOMEPAGE=              https://www.wireguard.com/

# GPLv2
PERMIT_PACKAGE=        Yes

WANTLIB=               c

USE_GMAKE=             Yes

# Uses __builtin_bswap* on big-endian archs
COMPILER=              base-clang ports-gcc

RUN_DEPENDS=           net/wireguard-go shells/bash

WRKBUILD=              ${WRKDIST}/src

MAKE_FLAGS=            WITH_WGQUICK=yes WITH_BASHCOMPLETION=yes
FAKE_FLAGS=            MANDIR="${PREFIX}/man" PREFIX="${PREFIX}"

NO_TEST=               Yes

ALL_TARGET=            tools
INSTALL_TARGET=        tools-install

post-extract:
	sed -i 's/install -v /install /g' ${WRKDIST}/src/tools/Makefile

.include <bsd.port.mk>
