TEXFILES = $(wildcard *.tex)
HTMLFILES = $(TEXFILES:%.tex=%.html)
PDFFILES = $(wildcard *.tex:%.tex=%.pdf)

all: $(HTMLFILES)

%.html: %.tex Makefile ipad.sty ipad.cfg
	htlatex $< "ipad,xhtml,jsmath,2" " -cmozhtf"

%.pdf: %.tex
	pdflatex $<

clean:
	rm -f *.4ct *.4tc *.aux *.dvi *.idv *.lg *.log *.out *.thm *.tmp *.xref
