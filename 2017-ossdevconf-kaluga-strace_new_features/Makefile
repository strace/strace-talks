PDF = ./ossdevconf_2017-slides-strace_new_features.pdf
INC = strace-straus-1781x3426.png
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
