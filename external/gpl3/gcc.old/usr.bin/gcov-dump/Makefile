#	$NetBSD: Makefile,v 1.1.1.1 2018/08/01 22:19:01 mrg Exp $

.include <bsd.init.mk>

PROG=           gcov-dump
SRCS=		${G_GCOV_DUMP_OBJS:.o=.c}

CPPFLAGS+=	-I${GCCARCH} -I${BACKENDOBJ} ${G_ALL_CFLAGS:M-D*} ${G_INCLUDES:M-I*:N-I.*}

BINDIR=		/usr/bin

MAN=		gcov-dump.1

HOSTPROG_CXX=	1

.include <bsd.prog.mk>

# Force using C++ for this
HOST_CC:=	${HOST_CXX}
CC:=		${CXX}
CFLAGS:=	${CXXFLAGS} -Wno-stack-protector

.include "../Makefile.common"
.include "../Makefile.libcpp"
.include "../Makefile.backtrace"
.include "../Makefile.libiberty"
.include "../Makefile.libdecnumber"

LDADD+=		-lintl
DPADD+=		${LIBINTL}

.PATH: ${DIST}/gcc ${DIST}/gcc/doc
