PDF = ./devconf_2023-slides-netlink-decoding-in-strace.pdf
INC = strace-straus.pdf nlmsg_example.pdf
VIEW = atril

.PHONY:	all clean distclean pdf view

all: pdf

view: pdf
	${VIEW} ${PDF}

pdf: ${PDF}

%.pdf: %.tex ${INC}
	pdflatex $< $@

%.pdf: %.svg
	rsvg-convert -f pdf -h 1080 -o $@ $<

distclean: clean
	rm -f ${PDF} ${INC}

clean:
	rm -f *.aux *.log *.nav *.out *.snm *.toc *.vrb
