NAME=proposal

LATEX=pdflatex 
#/usr/local/texlive/2014/bin/universal-darwin/pdflatex
BIBTEX=bibtex
#/usr/local/texlive/2014/bin/universal-darwin/bibtex

FILES = codes.tex macros.tex measurements.tex merit.tex objectives.tex motivation.tex people.tex prior_results.tex proposal.tex significance.tex simulations.tex timeline.tex title.tex galactic_measurements.tex


all:  $(NAME).pdf $(FILES)

dvi: $(NAME).tex
	$(LATEX) $(NAME) || true
	$(BIBTEX) $(NAME)
	$(LATEX) $(NAME) || true 
	$(BIBTEX) $(NAME)
	$(LATEX) $(NAME) || true 
	$(LATEX) $(NAME)

$(NAME).pdf: $(NAME).tex $(FILES)
	$(LATEX) $(NAME) 
	$(BIBTEX) $(NAME)
	$(LATEX) $(NAME) 
	$(LATEX) $(NAME) 
#	dvipdf $(NAME).dvi $(NAME).pdf
#	rm -f $(NAME).blg $(NAME).log $(NAME).aux

clean:
	rm -f *~ *.aux *.dvi *.gz *.out *.toc *log *-temp.* *.blg *~ $(NAME).ps $(NAME).bbl $(NAME).pdf

o: $(NAME).pdf
	open $(NAME).pdf
