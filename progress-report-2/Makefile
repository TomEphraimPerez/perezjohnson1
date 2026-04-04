.PHONY: all diagrams pdf clean

TEXCOMMAND=lualatex
ARGS=-interaction=batchmode -shell-escape
DOC_NAME=progress-report-2
DIAGRAM_NAME=classDiagram
DIAGRAM_OUT=$(DIAGRAM_NAME).png
RM=rm -f

all: diagrams pdf

diagrams: $(DIAGRAM_OUT)

$(DIAGRAM_OUT): $(DIAGRAM_NAME).plantuml
	plantuml -tpng $(DIAGRAM_NAME).plantuml

pdf: $(DOC_NAME).latex
	$(TEXCOMMAND) $(ARGS) $(DOC_NAME).latex

pdflog: $(DOC_NAME).latex
	$(TEXCOMMAND) $(DOC_NAME).latex

clean:
	$(RM) *.aux
	$(RM) *.log
	$(RM) *.pdf
	$(RM) *.blg
	$(RM) *.out
	$(RM) *.bbl
	$(RM) *.tikz
