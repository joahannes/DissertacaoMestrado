# Criação do Makefile:
# Guilherme Folego - 11.06.2015

# Adicao da opção para criar Lista de Abreviaturas via Makefile:
# Joahannes Costa - 19.03.2018

# pdflatex
LATEX=pdflatex
LATEXOPT=-interaction=nonstopmode -halt-on-error

# latexmk
LATEXMK=latexmk
LATEXMKOPT=-pdf -bibtex -quiet

# index
NAME="mestrado_joahannes"

# rules
all:
	$(LATEXMK) $(LATEXMKOPT) \
		-pdflatex="$(LATEX) $(LATEXOPT)"

clean:
	$(LATEXMK) $(LATEXMKOPT) -C
	rm -f *-eps-converted-to.pdf

index:
	makeindex -s nomencl.ist -t $(NAME).nlg -o $(NAME).nls $(NAME).nlo

clean_index:
	rm -f *.nlg
	rm -f *.nls
	rm -f *.nlo

.PHONY: all clean
