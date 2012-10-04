# $FreeBSD$

.if exists(../Makefile.conf)
.include "../Makefile.conf"
.endif
.if exists(../Makefile.inc)
.include "../Makefile.inc"
.endif

DOCS?=	index.xml

SUBDIR+=	9.1R

.if defined $(NEW_BUILD)
SUBDIR=
.endif

.include "${DOC_PREFIX}/share/mk/web.site.mk"
