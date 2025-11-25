# FPGA Vision Accelerators Survey (2013-2025)

**Comprehensive Survey on FPGA-based Computer Vision Accelerators**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**Author**: Mohammad Pivezhandi  
**Affiliation**: Wayne State University, Detroit, MI 48202

---

## Overview

This repository contains the LaTeX source for a comprehensive survey on FPGA implementations of computer vision accelerators, covering traditional feature extraction methods, deep learning architectures (CNNs, Vision Transformers), Edge AI/TinyML, and neuromorphic computing.

**Survey Coverage**: 102 papers with complete performance metrics (2013-2025)

---

## Quick Start

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

---

## Repository Structure

```
FPGA-Vision-Survey/
├── updated_survey/          # LaTeX survey source
│   ├── updated_survey.tex  # Main document
│   ├── Makefile            # Build automation
│   ├── sections/           # Modular LaTeX sections
│   │   ├── introduction.tex
│   │   ├── feature_extraction.tex
│   │   ├── neural_networks.tex
│   │   ├── transformers.tex         # Vision Transformers (NEW)
│   │   ├── edge_ai.tex             # Edge AI & TinyML (NEW)
│   │   ├── neuromorphic.tex
│   │   ├── conclusion.tex
│   │   └── updated_refs.bib        # Bibliography (102+ entries)
│   └── figures/            # 67 publication-quality figures
├── README.md
└── LICENSE
```

---

## Survey Highlights

### Research Areas

1. **Feature Extraction Methods**
   - Harris Corner Detection, SIFT, SURF

2. **Deep Learning Architectures**
   - CNNs: LeNet, AlexNet, VGG, ResNet, MobileNet, EfficientNet
   - Object Detection: YOLO series, SSD, Faster R-CNN

3. **Vision Transformers** ⭐ NEW
   - ViT, DeiT, Swin Transformer
   - Attention mechanism optimization

4. **Edge AI & TinyML** ⭐ NEW
   - Ultra-low-power implementations (<1W)
   - On-device learning

5. **Optimization Techniques**
   - Quantization, Pruning, Winograd/FFT
   - Hardware-aware NAS

6. **Neuromorphic Computing**
   - Spiking Neural Networks
   - Event-based vision

### Key Statistics

- **102 papers** with complete 23-metric dataset
- **67 figures** publication-quality
- **256 citations** comprehensive bibliography
- **2013-2025** coverage

---

## Citation

```bibtex
@misc{pivezhandi2024fpga,
  title={A Comprehensive Survey on FPGA-based Computer Vision Accelerators},
  author={Pivezhandi, Mohammad},
  year={2024},
  institution={Wayne State University}
}
```

---

## License

MIT License - See [LICENSE](LICENSE) for details.

---

## Contact

**Mohammad Pivezhandi**  
Wayne State University  
Detroit, MI 48202

---

**Note**: This is the public LaTeX source repository. Supporting materials (data files, source papers, analysis scripts) are available in a private repository for collaborators.
