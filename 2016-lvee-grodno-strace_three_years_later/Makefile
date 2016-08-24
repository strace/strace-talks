PDF = ./lvee_2016-abstract-strace_three_years_later.pdf
INC =
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
