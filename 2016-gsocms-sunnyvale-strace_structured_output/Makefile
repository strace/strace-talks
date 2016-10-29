PDF = ./gsoc_2016_ms-lt-slides-strace_structured_output.pdf
INC = lp0-conversion.pdf lp0-structured.pdf
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
