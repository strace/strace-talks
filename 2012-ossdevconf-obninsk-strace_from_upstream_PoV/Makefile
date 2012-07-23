PDF = ./ossdevconf_2012-slides-strace_from_upstream_PoV.pdf
INC = altlinux.png
VIEW = evince

.PHONY:	all clean distclean pdf view

view: all
	${VIEW} ${PDF}

all: pdf

pdf: ${PDF}

%.pdf: %.tex ${INC}
	pdflatex $< $@

distclean: clean
	rm -f ${PDF}

clean:
	rm -f *.aux *.log *.nav *.out *.snm *.toc *.vrb
