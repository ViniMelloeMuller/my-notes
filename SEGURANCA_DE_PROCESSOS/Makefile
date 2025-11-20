# Nome do arquivo principal (sem extensão)
MAIN = main

# Comando padrão
all: pdf

# Compilação simples em PDF
pdf:
	pdflatex $(MAIN).tex
	pdflatex $(MAIN).tex

# Compilação completa incluindo bibliografia (caso use BibTeX)
bib:
	pdflatex $(MAIN).tex
	bibtex $(MAIN)
	pdflatex $(MAIN).tex
	pdflatex $(MAIN).tex

# Remoção de arquivos temporários
clean:
	rm -f *.aux *.log *.out *.toc *.bbl *.blg *.lof *.lot *.fls *.fdb_latexmk

# Remove tudo, menos o PDF
cleanall: clean
	rm -f $(MAIN).pdf

# Visualizar PDF
view:
	open $(MAIN).pdf &

.PHONY: clean cleanall pdf view bib

