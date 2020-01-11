PDF = ./devconfcz_2020-slides-the_history_of_a_linux_kernel_design_flaw.pdf
INC = strace-straus.pdf devconfcz.pdf basealt.jpg tux.png wat.pdf kaleidoscope.jpg \
      indan.jpg linus.jpg hpa.jpg roland.jpg denys.jpg oleg.jpg pedro.jpg andy.jpg lp.jpg \
      paul.jpg andrew.jpg
VIEW = atril-previewer

.PHONY:	all clean distclean pdf view

view: all
	${VIEW} ${PDF}

all: pdf

pdf: ${PDF}

%.pdf: %.tex ${INC}
	pdflatex $< $@

%.pdf: %.svg
	rsvg-convert -f pdf -h 1080 -o $@ $<

distclean: clean
	rm -f ${PDF} ${INC}

clean:
	rm -f *.aux *.log *.nav *.out *.snm *.toc *.vrb
