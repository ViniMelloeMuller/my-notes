# Nome do arquivo principal (sem extensão)
MAIN = main

# Engine
ENGINE = lualatex

# Comando padrão
all: bib

# Compilação simples em PDF
pdf:
	$(ENGINE) $(MAIN).tex
	$(ENGINE) $(MAIN).tex

# Compilação completa incluindo bibliografia (caso use BibTeX)
bib:
	$(ENGINE) $(MAIN).tex
	biber $(MAIN)
	$(ENGINE) $(MAIN).tex
	$(ENGINE) $(MAIN).tex

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

