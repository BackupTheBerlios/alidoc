#
# $FreeBSD$
#
# Crea il Manuale di FreeBSD.
#

# ------------------------------------------------------------------------
#
# Variabili specifiche del Manuale
#
#       WITH_PGPKEYS    La versione stampata del manuale riporta solo i
#                       fingerprints PGP di base.  Se vuoi visualizzare
#                       le chiavi intere, allora setta questa variabile.
#                       Questa opzione non ha effetto sui formati HTML.
#
# Targets specifici del Manuale
#
#       pgpkeyring      Questo target legger� il contenuto del file
#                       pgpkeys/chapter.sgml ad estrarr� tutte le chiavi
#                       pgp sullo standard output.  Questo output pu�
#                       quindi essere rediretto su un file e distribuito
#                       come un keyring pubblico degli sviluppatori di
#                       FreeBSD che pu� essere facilmente importato in
#                       PGP/GPG.
#
# ------------------------------------------------------------------------

MAINTAINER= ale@FreeBSD.org

DOC?= book

FORMATS?= html-split

HAS_INDEX= true
WITH_GLOSSARY?=

INSTALL_COMPRESSED?= gz
INSTALL_ONLY_COMPRESSED?=

IMAGES_EN = advanced-networking/isdn-bus.eps
IMAGES_EN+= advanced-networking/isdn-twisted-pair.eps
IMAGES_EN+= advanced-networking/natd.eps
IMAGES_EN+= advanced-networking/net-routing.pic
IMAGES_EN+= install/adduser1.scr
IMAGES_EN+= install/adduser2.scr
IMAGES_EN+= install/adduser3.scr
IMAGES_EN+= install/boot-mgr.scr
IMAGES_EN+= install/console-saver1.scr
IMAGES_EN+= install/console-saver2.scr
IMAGES_EN+= install/console-saver3.scr
IMAGES_EN+= install/console-saver4.scr
IMAGES_EN+= install/desktop.scr
IMAGES_EN+= install/disklabel-auto.scr
IMAGES_EN+= install/disklabel-ed1.scr
IMAGES_EN+= install/disklabel-ed2.scr
IMAGES_EN+= install/disklabel-fs.scr
IMAGES_EN+= install/disklabel-root1.scr
IMAGES_EN+= install/disklabel-root2.scr
IMAGES_EN+= install/disklabel-root3.scr
IMAGES_EN+= install/disk-layout.eps
IMAGES_EN+= install/dist-set.scr
IMAGES_EN+= install/dist-set2.scr
IMAGES_EN+= install/docmenu1.scr
IMAGES_EN+= install/ed0-conf.scr
IMAGES_EN+= install/ed0-conf2.scr
IMAGES_EN+= install/edit-inetd-conf.scr
IMAGES_EN+= install/example-dir1.eps
IMAGES_EN+= install/example-dir2.eps
IMAGES_EN+= install/example-dir3.eps
IMAGES_EN+= install/example-dir4.eps
IMAGES_EN+= install/example-dir5.eps
IMAGES_EN+= install/fdisk-drive1.scr
IMAGES_EN+= install/fdisk-drive2.scr
IMAGES_EN+= install/fdisk-edit1.scr
IMAGES_EN+= install/fdisk-edit2.scr
IMAGES_EN+= install/ftp-anon1.scr
IMAGES_EN+= install/ftp-anon2.scr
IMAGES_EN+= install/hdwrconf.scr
IMAGES_EN+= install/keymap.scr
IMAGES_EN+= install/main1.scr
IMAGES_EN+= install/mainexit.scr
IMAGES_EN+= install/main-std.scr
IMAGES_EN+= install/main-options.scr
IMAGES_EN+= install/main-doc.scr
IMAGES_EN+= install/main-keymap.scr
IMAGES_EN+= install/media.scr
IMAGES_EN+= install/mouse1.scr
IMAGES_EN+= install/mouse2.scr
IMAGES_EN+= install/mouse3.scr
IMAGES_EN+= install/mouse4.scr
IMAGES_EN+= install/mouse5.scr
IMAGES_EN+= install/mouse6.scr
IMAGES_EN+= install/mta-main.scr
IMAGES_EN+= install/net-config-menu1.scr
IMAGES_EN+= install/net-config-menu2.scr
IMAGES_EN+= install/nfs-server-edit.scr
IMAGES_EN+= install/ntp-config.scr
IMAGES_EN+= install/options.scr
IMAGES_EN+= install/pkg-cat.scr
IMAGES_EN+= install/pkg-confirm.scr
IMAGES_EN+= install/pkg-install.scr
IMAGES_EN+= install/pkg-sel.scr
IMAGES_EN+= install/probstart.scr
IMAGES_EN+= install/routed.scr
IMAGES_EN+= install/security.scr
IMAGES_EN+= install/sysinstall-exit.scr
IMAGES_EN+= install/timezone1.scr
IMAGES_EN+= install/timezone2.scr
IMAGES_EN+= install/timezone3.scr
IMAGES_EN+= install/userconfig.scr
IMAGES_EN+= install/userconfig2.scr
IMAGES_EN+= install/xf86setup.scr
IMAGES_EN+= mail/mutt1.scr
IMAGES_EN+= mail/mutt2.scr
IMAGES_EN+= mail/mutt3.scr
IMAGES_EN+= mail/pine1.scr
IMAGES_EN+= mail/pine2.scr
IMAGES_EN+= mail/pine3.scr
IMAGES_EN+= mail/pine4.scr
IMAGES_EN+= mail/pine5.scr
IMAGES_EN+= security/ipsec-crypt-pkt.pic
IMAGES_EN+= security/ipsec-encap-pkt.pic
IMAGES_EN+= security/ipsec-network.pic
IMAGES_EN+= security/ipsec-out-pkt.pic
IMAGES_EN+= vinum/vinum-concat.pic
IMAGES_EN+= vinum/vinum-mirrored-vol.pic
IMAGES_EN+= vinum/vinum-raid10-vol.pic
IMAGES_EN+= vinum/vinum-raid5-org.pic
IMAGES_EN+= vinum/vinum-simple-vol.pic
IMAGES_EN+= vinum/vinum-striped-vol.pic
IMAGES_EN+= vinum/vinum-striped.pic

# Immagini dalla libreria per tutti i documenti
IMAGES_LIB = callouts/1.png
IMAGES_LIB+= callouts/2.png
IMAGES_LIB+= callouts/3.png
IMAGES_LIB+= callouts/4.png
IMAGES_LIB+= callouts/5.png
IMAGES_LIB+= callouts/6.png
IMAGES_LIB+= callouts/7.png
IMAGES_LIB+= callouts/8.png
IMAGES_LIB+= callouts/9.png
IMAGES_LIB+= callouts/10.png

#
# SRCS lista i singoli files SGML che compongono il documento. Modifiche
# a qualunque di questi files obbligano la ricreazione
#

# Contenuto SGML
SRCS = book.sgml
SRCS+= advanced-networking/chapter.sgml
SRCS+= basics/chapter.sgml
SRCS+= bibliography/chapter.sgml
SRCS+= config/chapter.sgml
SRCS+= boot/chapter.sgml
SRCS+= cutting-edge/chapter.sgml
SRCS+= desktop/chapter.sgml
SRCS+= disks/chapter.sgml
SRCS+= eresources/chapter.sgml
SRCS+= install/chapter.sgml
SRCS+= introduction/chapter.sgml
SRCS+= kernelconfig/chapter.sgml
SRCS+= l10n/chapter.sgml
SRCS+= linuxemu/chapter.sgml
SRCS+= mail/chapter.sgml
SRCS+= mirrors/chapter.sgml
SRCS+= multimedia/chapter.sgml
SRCS+= pgpkeys/chapter.sgml
SRCS+= ppp-and-slip/chapter.sgml
SRCS+= printing/chapter.sgml
SRCS+= security/chapter.sgml
SRCS+= serialcomms/chapter.sgml
SRCS+= users/chapter.sgml
SRCS+= vinum/chapter.sgml
SRCS+= x11/chapter.sgml
SRCS+= ports/chapter.sgml
SRCS+= preface/preface.sgml
SRCS+= colophon.sgml

# Entities
SRCS+= chapters.ent

SYMLINKS=	${DESTDIR} index.html handbook.html

# Attiva tutti i capitoli.
CHAPTERS?= ${SRCS:M*chapter.sgml}

SGMLFLAGS+= ${CHAPTERS:S/\/chapter.sgml//:S/^/-i chap./}
.if defined(WITH_GLOSSARY) && !empty(WITH_GLOSSARY)
SGMLFLAGS+= -i chap.freebsd-glossary
.endif

# XXX La creazione del Manuale attualmente sfora dei limiti interni,
# codificati in pdftex.  Finch� non dividiamo il Manuale, crea la versione
# PDF usando ps2pdf invece di pdftex.

PS2PDF?=	${PREFIX}/bin/ps2pdf

book.tex-pdf:
	${TOUCH} book.tex-pdf

book.pdf: book.ps
	${PS2PDF} book.ps book.pdf

pgpkeyring: pgpkeys/chapter.sgml
	@${JADE} -V nochunks ${JADEOPTS} -d ${DSLPGP} -t sgml ${MASTERDOC}

#
# Variabili specifiche del Manuale
#
.if defined(WITH_PGPKEYS)
JADEFLAGS+=	-V withpgpkeys
.endif

DOC_PREFIX?= ${.CURDIR}/../../..

.for p in ftp cvsup
SRCS+= mirrors.sgml.${p}.inc
CLEANFILES+= mirrors.sgml.${p}.inc
CLEANFILES+= mirrors.sgml.${p}.inc.tmp
.endfor

SRCS+= eresources.sgml.www.inc
CLEANFILES+= eresources.sgml.www.inc
CLEANFILES+= eresources.sgml.www.inc.tmp

.include "${DOC_PREFIX}/share/mk/doc.project.mk"

.for p in ftp cvsup
mirrors.sgml.${p}.inc: ${XML_MIRRORS} ${XSL_MIRRORS}
	${XSLTPROC} ${XSLTPROCOPTS} \
	    -o $@.tmp \
	    --param 'type' "'$p'" \
	    --param 'proto' "'$p'" \
	    --param 'target' "'handbook/mirrors/chapter.sgml'" \
	    ${XSL_MIRRORS} ${XML_MIRRORS}
	${SED} -e 's,<\([^ >]*\)\([^>]*\)/>,<\1\2></\1>,;s,</anchor>,,' \
	    < $@.tmp > $@ || (${RM} -f $@ && false)
	${RM} -f $@.tmp
.endfor

eresources.sgml.www.inc: ${XML_MIRRORS} ${XSL_MIRRORS}
	${XSLTPROC} ${XSLTPROCOPTS} \
	    -o $@.tmp \
	    --param 'type' "'www'" \
	    --param 'proto' "'http'" \
	    --param 'target' "'handbook/eresources/chapter.sgml'" \
	    ${XSL_MIRRORS} ${XML_MIRRORS}
	${SED} -e 's,<\([^ >]*\)\([^>]*\)/>,<\1\2></\1>,;s,</anchor>,,' \
	    < $@.tmp > $@ || (${RM} -f $@ && false)
	${RM} -f $@.tmp
