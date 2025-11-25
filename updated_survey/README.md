# FPGA Vision Accelerators Survey - LaTeX Source

This directory contains the LaTeX source files for the survey. It is kept compact for easy uploading to Overleaf.

## 📂 Contents

```
updated_survey/
├── updated_survey.tex    # Main LaTeX document
├── Makefile              # Build automation
├── sections/             # Modular LaTeX sections
│   ├── abstract.tex
│   ├── introduction.tex
│   ├── feature_extraction.tex
│   ├── neural_networks.tex
│   ├── transformers.tex
│   ├── edge_ai.tex
│   ├── spiking_networks.tex
│   ├── conclusion.tex
│   └── updated_refs.bib
└── figures/              # 67 figure files
```

## 🚀 Quick Start

### Build PDF

```bash
# Using Makefile (recommended)
make              # Full build with bibliography
make quick        # Fast build
make view         # Build and open PDF
make clean        # Clean auxiliary files

# Manual build
pdflatex updated_survey.tex
bibtex updated_survey
pdflatex updated_survey.tex
pdflatex updated_survey.tex
```

### Upload to Overleaf

```bash
# Create zip
zip -r ../updated_survey.zip .

# Upload to Overleaf
# Set main document: updated_survey.tex
# Compiler: pdfLaTeX
```

## 📚 Documentation

All comprehensive documentation is in the main repository directory:

- **`../README_COMPREHENSIVE.md`** - Complete guide with all information
- **`../REVISION_SUMMARY.md`** - Details of LaTeX revisions
- **`../REORGANIZATION_COMPLETE.md`** - Repository structure
- **`../material/README_MATERIAL.md`** - Data, scripts, and papers guide

## 📊 Data and Scripts

Data and scripts are in `../material/`:

- **Data**: `../material/data_updated/Total_Updated.csv` (102 papers)
- **Scripts**: `../material/scripts_updated/comparison_plots.py`
- **Papers**: `../material/Sources/` (166 papers organized by conference/year)

## 🔗 Key Links

- Main repository: `../`
- Data directory: `../material/data_updated/`
- Scripts directory: `../material/scripts_updated/`
- Source papers: `../material/Sources/`

---

**For complete documentation, see `../README_COMPREHENSIVE.md`**
