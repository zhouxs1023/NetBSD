#	$NetBSD: Makefile,v 1.5 2017/07/23 01:12:23 mrg Exp $

libiberty/libiberty.a:
	[ ! -d libiberty ] && mkdir libiberty || true
	(cd libiberty; \
		CC=${HOST_CC:Q} \
		CFLAGS=${HOST_CFLAGS:Q} \
		MAKE=${MAKE:Q} \
		CONFIG_SHELL=${HOST_SH:Q} \
		${HOST_SH} ${DIST}/libiberty/configure \
		&& CC=${HOST_CC:Q} CFLAGS=${HOST_CFLAGS:Q} ${MAKE})

cleandir:
	-rm -rf libiberty

depend dependall all: libiberty/libiberty.a

.include <bsd.prog.mk>
