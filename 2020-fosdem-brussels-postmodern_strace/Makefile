PDF = ./fosdem_2020-slides-postmodern_strace.pdf
INC = strace-straus.pdf fosdem.pdf basealt.jpg wat.pdf kaleidoscope.jpg
VIEW = atril-previewer

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
