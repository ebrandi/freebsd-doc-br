# $FreeBSD$

.if exists(Makefile.conf)
.include "Makefile.conf"
.endif
.if exists(../Makefile.inc)
.include "../Makefile.inc"
.endif

# These are turned into validated, normalized HTML files.

DOCS=  about.xml
DOCS+= administration.xml
DOCS+= applications.xml
DOCS+= art.xml
DOCS+= availability.xml
DOCS+= docs.xml
DOCS+= features.xml
DOCS+= internet.xml
DOCS+= logo.xml
DOCS+= mailto.xml
DOCS+= privacy.xml
DOCS+= publish.xml
DOCS+= relnotes.xml
DOCS+= send-pr.xml
DOCS+= support.xml
DOCS+= where.xml

XMLDOCS=	index:xsl:${XML_NEWS_NEWS}:
DEPENDSET.index=transtable mirrors news press events \
		advisories notices

XMLDOCS+=	usergroups:${XSL_USERGROUPS}:${XML_USERGROUPS}:
DEPENDSET.usergroups=transtable usergroups
PARAMS.usergroups=	--param pagename "'FreeBSD User Groups'"

XMLDOCS+=	community::${XML_EVENTS_EVENTS}:
DEPENDSET.community=usergroups events

# These will be directly installed.

DATA=	favicon.ico
DATA+=	freebsd.css
DATA+=	index.css
DATA+=	robots.txt
DATA+=	vendors.html

# Subdirectories
# SGML
SUBDIR= FAQ
SUBDIR+= advocacy
SUBDIR+= commercial
SUBDIR+= community
SUBDIR+= copyright
SUBDIR+= developers
SUBDIR+= docproj
SUBDIR+= docs
SUBDIR+= donations
SUBDIR+= events
SUBDIR+= gnome
SUBDIR+= handbook
SUBDIR+= internal
SUBDIR+= ipv6
SUBDIR+= java
SUBDIR+= marketing
SUBDIR+= multimedia
SUBDIR+= news
SUBDIR+= platforms
SUBDIR+= portmgr
SUBDIR+= projects
SUBDIR+= prstats
SUBDIR+= releases
SUBDIR+= releng
SUBDIR+= search
SUBDIR+= security
SUBDIR+= snapshots
SUBDIR+= support
SUBDIR+= tutorials
.if !defined(WEB_ONLY) || empty(WEB_ONLY)
SUBDIR+= doc
SUBDIR+= ports
.endif
.if defined(BUILD_RELNOTES)
SUBDIR+= relnotes
.endif

# Non-SGML
SUBDIR+= cgi
SUBDIR+= gifs
SUBDIR+= layout
SUBDIR+= logo

.if !defined(WEB_LANG) || empty(WEB_LANG)
WEB_LANG=	pt_BR.ISO8859-1 
.endif
.if !defined(ENGLISH_ONLY) || empty(ENGLISH_ONLY)
.for _D in ${WEB_LANG}
SUBDIR+=	../../${_D}/htdocs
.endfor
.endif

WEBDIR?=	data

.include "${DOC_PREFIX}/share/mk/web.site.mk"
