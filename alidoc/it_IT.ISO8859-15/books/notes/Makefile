#
# $FreeBSD$
#
# Crea Note su FreeBSD.
#

MAINTAINER= ale@FreeBSD.org

DOC?= book

FORMATS?= html-split

INSTALL_COMPRESSED?= gz
INSTALL_ONLY_COMPRESSED?=

#
# SRCS lista i singoli files SGML che compongono il documento. Modifiche
# a qualunque di questi files obbligano la ricreazione
#

# Contenuto SGML
SRCS = book.sgml
SRCS+= preface/preface.sgml
SRCS+= bsd/chapter.sgml
SRCS+= freebsd/chapter.sgml
SRCS+= ports/chapter.sgml
SRCS+= kernel/chapter.sgml
SRCS+= update/chapter.sgml
SRCS+= activities/chapter.sgml
SRCS+= apache2/chapter.sgml

# Entities
SRCS+= chapters.ent

DOC_PREFIX?= 	${.CURDIR}/../../..
.include "${DOC_PREFIX}/share/mk/doc.project.mk"
