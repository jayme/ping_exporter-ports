# $FreeBSD: head/sysutils/ping_exporter/Makefile

PORTNAME=       ping_exporter
DISTVERSION=    0.44
CATEGORIES=     sysutils

MAINTAINER=     jp+ports@supplntr.io
COMMENT=        Prometheus exporter for ICMP echo requests using https://github.com/digineo/go-ping

LICENSE=        APACHE20

ONLY_FOR_ARCHS= amd64

USES=           go
USE_GITHUB=     yes
GH_PROJECT=     ping_exporter
GH_ACCOUNT=     czerwonk

GO_PKGNAME=     github.com/${GH_ACCOUNT}/${GH_PROJECT}

PLIST_FILES=    bin/ping_exporter \
                etc/ping_exporter.yml.sample

USE_RC_SUBR=    ping_exporter

.include <bsd.port.options.mk>

post-install:
	${INSTALL_DATA} ${PATCHDIR}/ping_exporter.yml.sample \
	${STAGEDIR}${PREFIX}/etc/ping_exporter.yml.sample

.include <bsd.port.mk>
