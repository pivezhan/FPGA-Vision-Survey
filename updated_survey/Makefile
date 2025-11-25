# Makefile for FPGA Vision Accelerators Survey
# Compiles updated_survey.tex to PDF
#
# Usage:
#   make          - Build PDF (full compilation with bibliography)
#   make quick    - Quick build (single pdflatex pass)
#   make clean    - Remove auxiliary files
#   make distclean - Remove all generated files including PDF
#   make view     - Open PDF viewer (Linux)
#   make help     - Show this help message

# Configuration
MAIN = updated_survey
TEX = $(MAIN).tex
PDF = $(MAIN).pdf
BBL = $(MAIN).bbl
BIB = sections/updated_refs.bib

# LaTeX compiler and flags
LATEX = pdflatex
BIBTEX = bibtex
LATEX_FLAGS = -interaction=nonstopmode -file-line-error

# PDF viewer (change based on your system)
PDF_VIEWER = evince

# All section files
SECTIONS = sections/abstract.tex \
           sections/introduction.tex \
           sections/feature_extraction.tex \
           sections/neural_networks.tex \
           sections/transformers.tex \
           sections/edge_ai.tex \
           sections/spiking_networks.tex \
           sections/conclusion.tex

# All figures
FIGURES = $(wildcard figures/*.pdf) $(wildcard figures/*.png) $(wildcard figures/*.jpg)

.PHONY: all quick clean distclean view help

# Default target: full compilation with bibliography
all: $(PDF)

# Full compilation: LaTeX -> BibTeX -> LaTeX -> LaTeX
$(PDF): $(TEX) $(SECTIONS) $(BIB) $(FIGURES)
	@echo "=== Building $(MAIN).pdf with full compilation ==="
	@echo "Step 1/4: First pdflatex pass..."
	$(LATEX) $(LATEX_FLAGS) $(TEX)
	@echo ""
	@echo "Step 2/4: Running bibtex..."
	-$(BIBTEX) $(MAIN) || true
	@echo ""
	@echo "Step 3/4: Second pdflatex pass..."
	$(LATEX) $(LATEX_FLAGS) $(TEX)
	@echo ""
	@echo "Step 4/4: Third pdflatex pass..."
	$(LATEX) $(LATEX_FLAGS) $(TEX)
	@echo ""
	@echo "=== Build complete! ==="
	@echo "Output: $(PDF)"
	@ls -lh $(PDF)

# Quick build: single pdflatex pass (useful for draft edits)
quick: $(TEX) $(SECTIONS) $(FIGURES)
	@echo "=== Quick build: single pdflatex pass ==="
	$(LATEX) $(LATEX_FLAGS) $(TEX)
	@echo "=== Quick build complete! ==="
	@ls -lh $(PDF)

# Clean auxiliary files
clean:
	@echo "=== Cleaning auxiliary files ==="
	rm -f *.aux *.log *.out *.toc *.lof *.lot *.bbl *.blg *.synctex.gz *.fls *.fdb_latexmk
	rm -f sections/*.aux
	@echo "=== Clean complete ==="

# Remove all generated files including PDF
distclean: clean
	@echo "=== Removing PDF ==="
	rm -f $(PDF)
	@echo "=== Distclean complete ==="

# View PDF
view: $(PDF)
	@echo "=== Opening PDF viewer ==="
	@if command -v $(PDF_VIEWER) > /dev/null; then \
		$(PDF_VIEWER) $(PDF) & \
	elif command -v xdg-open > /dev/null; then \
		xdg-open $(PDF) & \
	else \
		echo "Error: No PDF viewer found. Install evince or set PDF_VIEWER in Makefile"; \
		exit 1; \
	fi

# Help message
help:
	@echo "FPGA Vision Accelerators Survey - Makefile"
	@echo ""
	@echo "Available targets:"
	@echo "  make           - Build PDF with full compilation (pdflatex + bibtex + pdflatex x2)"
	@echo "  make quick     - Quick build (single pdflatex pass, no bibliography update)"
	@echo "  make clean     - Remove auxiliary files (.aux, .log, .bbl, etc.)"
	@echo "  make distclean - Remove all generated files including PDF"
	@echo "  make view      - Open PDF in viewer (evince/xdg-open)"
	@echo "  make help      - Show this help message"
	@echo ""
	@echo "Files:"
	@echo "  Main document: $(TEX)"
	@echo "  Bibliography:  $(BIB)"
	@echo "  Output PDF:    $(PDF)"
	@echo ""
	@echo "Typical workflow:"
	@echo "  1. Edit LaTeX files in sections/"
	@echo "  2. Run 'make' for full build"
	@echo "  3. Run 'make view' to preview PDF"
	@echo "  4. For quick edits, use 'make quick' (faster)"
	@echo ""
	@echo "Notes:"
	@echo "  - First build requires full compilation for bibliography"
	@echo "  - After adding/changing citations, run full 'make'"
	@echo "  - For text-only edits, 'make quick' is sufficient"
	@echo "  - Data files are in ../material/data_updated/"
	@echo "  - Scripts are in ../material/scripts_updated/"
