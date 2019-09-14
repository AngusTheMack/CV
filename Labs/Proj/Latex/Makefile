# Makefile that deletes all the extra files
#all:
#	pdflatex  -bibtex -synctex=1 -interaction=nonstopmode -file-line-error -recorder -output-directory="."  "template.tex"

.PHONY: clean
clean:
	-rm -f *.aux
	-rm -f *.log
	-rm -f *.toc
	-rm -f *.bbl
	-rm -f *.blg
	-rm -f *.out
	-rm -f *.dvi
	-rm -f *.fls
	-rm -f *.fdb_latexmk
	-rm -f *.synctex.gz

.PHONY: cleanall
cleanall: clean
	-rm -f *.pdf
	-rm -f *.ps