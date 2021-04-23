SHELL=/bin/bash -O expand_aliases
DOCNAME=main

# --
# Master recipes
all: copy_bib clean tex 

clean: clean_tex

# --
# Sync the bib file from Zotero w/ this
# directory
copy_bib:
	cp ~/Documents/Papers/library.bib . 

# Compile the paper into pdf
# or clean up a compilations
tex:
	pdflatex $(DOCNAME).tex
	bibtex $(DOCNAME).aux
	pdflatex $(DOCNAME).tex
	pdflatex $(DOCNAME).tex

tex_nonstopmode:
	pdflatex -interaction=nonstopmode $(DOCNAME).tex
	bibtex $(DOCNAME).aux
	pdflatex -interaction=nonstopmode $(DOCNAME).tex
	pdflatex -interaction=nonstopmode $(DOCNAME).tex
	
tex2:
	latexmk $(DOCNAME).tex

clean_tex:
	# Spare the generate pdf...
	-mv $(DOCNAME).pdf tmp.pdf
	latexmk -C
	-mv tmp.pdf $(DOCNAME).pdf 
	-rm tmp.pdf
	# Other debris
	-rm *md5
	-rm *.log
	-rm *.aux
	-rm *.bbl
	-rm *dpth
	-rm *suppinfo
	-rm *.auxlock
	-rm __latexindent_temp.tex

# rm the pdf, just in case. 
# the normal clean_tex leaves the
# pdflatex output intact. 
# ...Sometimes this is not helpful.
clean_pdf:
	-rm $(DOCNAME).pdf 
	