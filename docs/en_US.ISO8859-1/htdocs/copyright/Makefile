# $FreeBSD$

.if exists(../Makefile.conf)
.include "../Makefile.conf"
.endif
.if exists(../Makefile.inc)
.include "../Makefile.inc"
.endif

DOCS=	copyright.xml
DOCS+=	daemon.xml
DOCS+=	freebsd-doc-license.xml
DOCS+=	freebsd-license.xml
DOCS+=	license.xml
DOCS+=	trademarks.xml

INDEXLINK= copyright.html

DATA+= COPYING COPYING.LIB LEGAL

CLEANFILES+= LEGAL

LEGAL:
	${FETCH} http://svn.freebsd.org/ports/head/LEGAL

.include "${DOC_PREFIX}/share/mk/web.site.mk"
