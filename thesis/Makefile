PAPER = pacora-isca13
TEX = $(wildcard *.tex)
BIB = references.bib
FIGS = $(wildcard figures/*.pdf figures/*.png graphs/*.pdf graphs/*.png)

all: $(PAPER).pdf

.PHONY: all clean

open: all
	open $(PAPER).pdf

$(PAPER).pdf: $(TEX) $(BIB) $(FIGS) ucbthesis.cls
	echo $(FIGS)
	pdflatex $(PAPER)
	bibtex $(PAPER)
	pdflatex $(PAPER)
	pdflatex $(PAPER)

once:
	pdflatex $(PAPER)


clean:
	rm -f *.aux *.bbl *.blg *.log *.out $(PAPER).pdf

