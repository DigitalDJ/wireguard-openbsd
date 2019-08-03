# $OpenBSD$
ONLY_FOR_ARCHS=        amd64

COMMENT=               fast, modern, secure VPN tunnel (Go)

VERSION=               0.0.20190517

DISTNAME=              wireguard-go-${VERSION}

CATEGORIES=            net security
MASTER_SITES=          https://git.zx2c4.com/wireguard-go/snapshot/
EXTRACT_SUFX=          .tar.xz

HOMEPAGE=              https://www.wireguard.com/

# GPLv2
PERMIT_PACKAGE=        Yes

WANTLIB=               c pthread

USE_GMAKE=             Yes

BUILD_DEPENDS=         lang/go devel/git

FAKE_FLAGS=            DESTDIR=""

post-extract:
	sed -i 's/install -v/install/g;s/@install/install/g' ${WRKDIST}/Makefile

.include <bsd.port.mk>
