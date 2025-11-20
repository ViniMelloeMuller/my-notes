# Nome do arquivo principal (sem extensão)
MAIN = main

# Comando padrão
all: bib

# Compilação simples em PDF
pdf:
	pdflatex $(MAIN).tex
	pdflatex $(MAIN).tex

# Compilação completa incluindo bibliografia (caso use BibTeX)
bib:
	pdflatex $(MAIN).tex
	biber $(MAIN)
	pdflatex $(MAIN).tex
	pdflatex $(MAIN).tex

# Remoção de arquivos temporários
clean:
	rm -f *.aux *.log *.out *.toc *.bbl *.blg *.lof *.lot *.fls *.fdb_latexmk *.bcf *.run.xml

# Remove tudo, menos o PDF
cleanall: clean
	rm -f $(MAIN).pdf

# Visualizar PDF
view:
	open $(MAIN).pdf &

.PHONY: clean cleanall pdf view bib

