# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**FPGA Vision Accelerators Survey**: A comprehensive survey on FPGA-based computer vision accelerators covering traditional feature extraction, deep learning (CNNs), vision transformers, edge AI/TinyML, and neuromorphic computing.

**Author**: Mohammad Pivezhandi
**Affiliation**: Wayne State University, Detroit, MI 48202
**Coverage**: 102 papers with complete performance metrics (2013-2025)

## Repository Structure

```
FPGA-Vision-Survey/
├── updated_survey/              # LaTeX survey source
│   ├── updated_survey.tex      # Main document
│   ├── updated_survey.pdf      # Compiled PDF
│   ├── Makefile                # Build automation
│   ├── IEEEtran.cls           # IEEE transaction style
│   ├── presentation.tex        # Survey presentation slides
│   ├── sections/               # Modular LaTeX sections
│   │   ├── abstract.tex       # Survey abstract
│   │   ├── introduction.tex   # Introduction and objectives
│   │   ├── feature_extraction.tex  # SIFT, HOG, SURF, etc.
│   │   ├── neural_networks.tex     # CNNs (739 lines - largest section)
│   │   ├── transformers.tex        # Vision Transformers (NEW)
│   │   ├── edge_ai.tex            # Edge AI & TinyML (NEW)
│   │   ├── spiking_networks.tex   # Neuromorphic computing
│   │   ├── conclusion.tex         # Conclusions
│   │   └── updated_refs.bib       # Bibliography (211+ entries)
│   └── figures/                # 67 publication-quality figures
├── README.md
├── LICENSE
├── CLAUDE.md                   # This file
└── SESSION_LOG.md              # Revision tracking
```

## Build Commands

### Build the Survey

```bash
cd updated_survey/
make
```

### Manual Build

```bash
cd updated_survey/
pdflatex updated_survey.tex
bibtex updated_survey
pdflatex updated_survey.tex
pdflatex updated_survey.tex
```

### Clean Build Artifacts

```bash
cd updated_survey/
make clean
```

## Survey Sections

| Section | File | Lines | Description |
|---------|------|-------|-------------|
| Abstract | abstract.tex | 7 | Survey scope and contributions |
| Introduction | introduction.tex | 19 | Background and objectives |
| Feature Extraction | feature_extraction.tex | 140 | SIFT, HOG, SURF, Harris |
| Neural Networks | neural_networks.tex | 739 | CNNs, object detection, optimization |
| Vision Transformers | transformers.tex | 112 | ViT, DeiT, Swin (NEW) |
| Edge AI | edge_ai.tex | 186 | TinyML, low-power implementations (NEW) |
| Spiking Networks | spiking_networks.tex | 24 | Neuromorphic computing |
| Conclusion | conclusion.tex | 2 | Summary and future directions |

## Revision Tracking Macros

The survey uses color-coded macros to track revisions:

```latex
\rev{...}       % NEW content (2019-2025) - displayed in RED
\revb{...}      % Grammatical revisions - displayed in BLUE
\newmetric{...} % New comparison metrics - displayed in BLUE
```

To disable colors for final submission, uncomment in `updated_survey.tex`:
```latex
\renewcommand{\rev}[1]{#1}
\renewcommand{\revb}[1]{#1}
\renewcommand{\newmetric}[1]{#1}
```

## Key Survey Topics

### 1. Feature Extraction Methods
- Harris Corner Detection
- SIFT (Scale-Invariant Feature Transform)
- SURF (Speeded-Up Robust Features)
- HOG (Histogram of Oriented Gradients)
- ORB (Oriented FAST and Rotated BRIEF)

### 2. Deep Learning Architectures
- **Classification**: LeNet, AlexNet, VGG, ResNet, MobileNet, EfficientNet
- **Object Detection**: YOLO series, SSD, Faster R-CNN
- **Optimization**: Quantization, Pruning, Winograd/FFT transforms

### 3. Vision Transformers (NEW Section)
- ViT (Vision Transformer)
- DeiT (Data-efficient Image Transformers)
- Swin Transformer
- Attention mechanism optimization for FPGAs

### 4. Edge AI & TinyML (NEW Section)
- Ultra-low-power implementations (<1W)
- On-device learning
- Hardware-aware neural architecture search

### 5. Neuromorphic Computing
- Spiking Neural Networks (SNNs)
- Event-based vision processing
- Bio-inspired implementations

## Key Statistics

- **102 papers** with complete 23-metric performance dataset
- **67 figures** publication-quality
- **211+ citations** in bibliography
- **2013-2025** coverage period
- **~1,229 lines** of LaTeX content

## FPGA Platforms Covered

- Xilinx: Zynq, Kintex, Virtex UltraScale+, Alveo
- Intel: Stratix, Arria, Agilex
- AMD: Versal (NEW)
- Low-power: Artix, Spartan

## Comparison Metrics

The survey evaluates implementations across 23 metrics including:
- Throughput (GOPS, FPS)
- Power consumption (W)
- Energy efficiency (GOPS/W)
- Resource utilization (LUTs, DSPs, BRAM)
- Latency (ms)
- Accuracy (Top-1, Top-5)

## Important Notes

### Revision Status
- The survey contains extensive revision markers (`\rev{}`, `\revb{}`)
- 259 NEW content markers (red)
- 100+ grammatical revision markers (blue)
- NEW sections: Vision Transformers, Edge AI

### Bibliography
- Located in `sections/updated_refs.bib`
- 211+ entries covering 2013-2025
- Use `ieeetr` bibliography style

### Figures
- 67 figures in `figures/` directory
- Mix of PDF and JPG formats
- Include comparison charts, architectures, and algorithm visualizations

## Related Work

This survey complements existing surveys:
- Venieris et al. (Toolflows for mapping CNNs)
- Wang et al. (DNN accelerator survey)
- Abdelouahab et al. (Accelerating CNNs)
- Guo et al. (Survey on DNN hardware accelerators)
