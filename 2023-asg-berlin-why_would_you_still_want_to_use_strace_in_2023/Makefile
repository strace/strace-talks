PDF = ./asg_2023-why_would_you_still_want_to_use_strace_in_2023.pdf
INC = strace-straus.pdf asg.jpg
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
