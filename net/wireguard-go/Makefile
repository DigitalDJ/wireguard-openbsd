# $OpenBSD$
COMMENT=               simple, fast and modern VPN implemented (Go)

VERSION=               0.0.20181222

DISTNAME=              wireguard-go-${VERSION}

CATEGORIES=            net security
MASTER_SITES=          https://git.zx2c4.com/wireguard-go/snapshot/
EXTRACT_SUFX=          .tar.xz

HOMEPAGE=              https://www.wireguard.com/

# GPLv2
PERMIT_PACKAGE_CDROM=  Yes

WANTLIB=               c

USE_GMAKE=             Yes

BUILD_DEPENDS=         lang/go devel/git

FAKE_FLAGS=            DESTDIR=""

post-extract:
	sed -i 's/install -v/install/g;s/@install/install/g' ${WRKDIST}/Makefile

.include <bsd.port.mk>
