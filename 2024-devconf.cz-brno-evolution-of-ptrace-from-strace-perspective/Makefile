PDF = ./devconfcz_2024-slides-evolution_of_ptrace_from_strace_perspective.pdf
INC = strace-straus.pdf devconf-cz-icon.pdf devconf-cz.pdf wat.pdf
VIEW = evince

.PHONY:	all clean distclean pdf view

view: all
	${VIEW} ${PDF}

all: pdf

pdf: ${PDF}

%.pdf: %.tex ${INC}
	pdflatex $< $@

%.pdf: %.svg
	rsvg-convert -f pdf -o $@ $<

distclean: clean
	rm -f ${PDF} ${INC}

clean:
	rm -f *.aux *.log *.nav *.out *.snm *.toc *.vrb
