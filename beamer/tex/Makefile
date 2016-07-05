# Makefile for dvips
# author Victor Pereira
# make PAPER=paper.tex

all:  $(addsuffix .ps,$(basename $(PAPER))) # text.ps
	ps2pdf $^

%.ps:  $(addsuffix .dvi,$(basename $(PAPER))) # text.dvi 
	dvips $^
    
%.dvi: $(PAPER)
#   latex $^ && bibtex $(basename $^) && latex $^ && latex $^ 
# without bibtex

	latex $^ && latex $^ && latex $^ 


#alternatively, if I do not want to use a specific file name
# Makefile for dvips
# build my pdf based on tex
# to build it:
# make 

#all: paper.ps
#	ps2pdf paper.ps

#paper.ps: paper.dvi 
#	dvips paper.dvi
    
#paper.dvi: paper.tex 
#	latex paper.tex && bibtex paper && latex paper.tex && latex paper.tex 
