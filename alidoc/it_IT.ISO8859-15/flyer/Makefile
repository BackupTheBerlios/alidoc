# $FreeBSD: doc/it_IT.ISO8859-15/flyer/Makefile,v 1.1 2004/01/26 18:20:06 ale Exp $

pdf: dvi ps
	ps2pdf13 -sPAPERSIZE=a4 flyer.ps

ps: dvi
	dvips -t a4 flyer.dvi -o

dvi: flyer.tex
	latex flyer.tex

clean:
	rm -f flyer.aux flyer.dvi flyer.log flyer.pdf flyer.ps