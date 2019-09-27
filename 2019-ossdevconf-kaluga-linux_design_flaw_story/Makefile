PDF = ./ossdevconf_2019-slides-linux_design_flaw_story.pdf
INC = strace-straus.pdf ossdevconf-logo.pdf basealt.jpg lineprinter.png tux-flat.png
VIEW = evince

.PHONY:	all clean distclean pdf view

view: all
	${VIEW} ${PDF}

all: pdf

pdf: ${PDF}

%.pdf: %.tex ${INC}
	pdflatex $< $@

%.pdf: %.svg
	rsvg-convert -f pdf -h 300 -o $@ $<

distclean: clean
	rm -f ${PDF} ${INC}

clean:
	rm -f *.aux *.log *.nav *.out *.snm *.toc *.vrb
