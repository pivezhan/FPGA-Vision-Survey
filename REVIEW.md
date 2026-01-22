# Comprehensive Review: FPGA Vision Accelerators Survey

**Reviewer Date:** 2026-01-21
**Target Venue:** ACM TRETS (Primary) or IEEE TCSVT (Backup)

---

## EXECUTIVE SUMMARY

| Category | Status | Priority |
|----------|--------|----------|
| Content Completeness | Good (85%) | Medium |
| Technical Accuracy | Good | Low |
| Writing Quality | Needs Work | **HIGH** |
| LaTeX/Formatting | Critical Issues | **HIGH** |
| Bibliography | Needs Cleanup | **HIGH** |
| Figures/Tables | Good | Low |

**Overall Assessment:** The survey is comprehensive with strong technical content covering 102 papers (2013-2025). However, significant revision is needed for:
1. LaTeX errors (duplicate labels, missing references)
2. Author information (commented out)
3. Bibliography cleanup (14 bibtex warnings)
4. Revision markers need removal for submission
5. Several new sections lack complete citations

---

## CRITICAL ISSUES (Must Fix)

### 1. LaTeX Errors

**Duplicate Labels:**
```
LaTeX Warning: Label `FeaturesDNN' multiply defined.
LaTeX Warning: Label `ResNet' multiply defined.
```
- `FeaturesDNN` appears in both neural_networks.tex and elsewhere
- `ResNet` label is used twice

**Action:** Rename duplicate labels to unique identifiers.

### 2. Undefined Reference
```
LaTeX Warning: Reference `neurochips' on page 28 undefined
```
- Line 8 of spiking_networks.tex references `\ref{neurochips}` but no figure/table has this label

**Action:** Either add the neurochips figure or remove the reference.

### 3. Author Information Missing
```latex
% \author{\IEEEauthorblockN{Mohammad Pivezhandi}
% \IEEEauthorblockA{...}
```
The author block is commented out in `updated_survey.tex` line 54-58.

**Action:** Uncomment and complete author information for submission.

### 4. Math Mode Warning
```
LaTeX Warning: Command \textendash invalid in math mode on input line 21.
```
In feature_extraction.tex, equation around line 21 has invalid `--` in math mode.

**Action:** Check equation formatting.

---

## HIGH PRIORITY ISSUES

### 5. Bibliography Cleanup (14 Warnings)

| Citation | Issue |
|----------|-------|
| harris1988combined | Both volume and number fields used |
| lowe2004distinctive | Empty booktitle + volume/number conflict |
| bay2008speeded | Empty booktitle + volume/number conflict |
| nair2010rectified | Empty journal |
| szegedy2015going | Empty booktitle |
| krizhevsky2009learning | Empty journal |
| zhou2017incremental | Empty booktitle |
| ma2019scalable | Empty journal |
| wang2016liquid | Empty journal |
| lammie2018unsupervised | Empty journal |
| mostafa2017fast | Empty journal |
| rios2015real | Empty journal |

**Action:** Fix all bibliography entries in `sections/updated_refs.bib`.

### 6. Revision Markers Active

The document uses color-coded revision markers:
- `\rev{...}` - 259 instances (red - new content)
- `\revb{...}` - 100+ instances (blue - grammatical revisions)

**Action:** For final submission, uncomment lines 10-12 in `updated_survey.tex`:
```latex
\renewcommand{\rev}[1]{#1}
\renewcommand{\revb}[1]{#1}
\renewcommand{\newmetric}[1]{#1}
```

### 7. Missing/Incomplete Citations in NEW Sections

Several NEW section citations appear to be placeholder-style:
- Vision Transformers section: `ham2021vita`, `you2022autoviT`, `park2023flightbert` - need verification
- Edge AI section: Several 2023-2024 citations need DOI/venue verification

**Action:** Verify all citations in new sections have complete information.

---

## MEDIUM PRIORITY ISSUES

### 8. Spiking Networks Section - Incomplete

The spiking networks section (24 lines) is significantly shorter than other sections:
- Neural Networks: 739 lines
- Transformers: 112 lines
- Edge AI: 186 lines
- Spiking Networks: 24 lines

**Recommendation:** Expand with:
- Recent FPGA implementations of SNNs (2021-2025)
- Comparison table like other sections
- Discussion of Intel Loihi, IBM TrueNorth FPGA alternatives

### 9. Abstract Needs Update

Current abstract claims coverage "from 2015 to 2025" but:
- Abstract mentions 2015 start, bibliography has papers from 2013
- Some NEW sections add 2023-2025 content

**Action:** Verify and update coverage claims in abstract.

### 10. Introduction Objectives

The introduction lists 4 objectives but the conclusion doesn't explicitly address each one:
1. ✓ Comprehensive analysis of vision algorithms
2. ✓ Coverage of top FPGA conferences
3. ⚠ Comparison tables exist but scattered
4. ⚠ Conclusions on optimal algorithms - could be strengthened

**Action:** Add a summary table in conclusion addressing all objectives.

### 11. Conclusion Too Short

The conclusion (3 lines) is minimal for a comprehensive survey.

**Recommendation:** Expand to include:
- Summary of key findings per section
- Quantitative comparison summary
- Explicit future research directions
- Recommendations for practitioners

---

## LOW PRIORITY ISSUES

### 12. Figure Quality Notes

- `NeuralProcessing.pdf` - PDF inclusion warning (may be minor)
- `keypointdescriptor.pdf` - PDF inclusion warning

**Action:** Check PDF figures for compatibility issues.

### 13. Table Formatting

Tables in Vision Transformers and Edge AI sections are well-formatted. Consider adding:
- Resource utilization columns (LUTs, DSPs, BRAM)
- Energy efficiency (GOPs/W) comparison across ALL sections

### 14. Section Balance

| Section | Lines | % of Total |
|---------|-------|------------|
| Feature Extraction | 140 | 11% |
| Neural Networks | 739 | 60% |
| Transformers | 112 | 9% |
| Spiking Networks | 24 | 2% |
| Edge AI | 186 | 15% |
| Other (intro/abstract/conclusion) | 28 | 2% |

The Neural Networks section dominates. Consider:
- Moving some subsections to an appendix
- Or splitting into "Classic CNNs" and "Modern Architectures"

---

## CONTENT REVIEW

### Strengths

1. **Comprehensive Coverage**: 102 papers with 23-metric comparisons
2. **NEW Sections**: Vision Transformers and Edge AI are timely additions
3. **Strong Technical Depth**: Detailed explanations of algorithms (SIFT, SURF, Winograd, etc.)
4. **Good Comparison Figures**: Resource/throughput comparisons across implementations
5. **Clear Organization**: Logical flow from feature extraction → DNNs → transformers → neuromorphic

### Weaknesses

1. **Spiking Networks Underdeveloped**: Needs expansion
2. **Conclusion Minimal**: Doesn't summarize key findings
3. **Missing Unified Comparison**: No single table comparing ALL approaches
4. **Object Detection Coverage**: YOLO section could be expanded
5. **No Reproducibility Discussion**: Missing discussion of open-source tools/frameworks

### Missing Topics (Consider Adding)

1. **Design Automation Tools**: FINN, Vitis AI, TVM - brief survey
2. **Emerging Architectures**: Spatial computing, near-memory computing
3. **Benchmarking Standards**: MLPerf, DAWNBench results on FPGAs
4. **Security**: Side-channel attacks on FPGA accelerators
5. **Multi-FPGA Systems**: Distributed acceleration

---

## VENUE-SPECIFIC REQUIREMENTS

### For ACM TRETS

- Contact Editor-in-Chief before submission with outline
- Comprehensive surveys welcome but require pre-approval
- No strict page limit (typical surveys: 30-50 pages)
- Need to differentiate from existing TRETS surveys (cite "A Survey of FPGA-based Neural Network Inference Accelerators")

### For IEEE TCSVT

- 14-page limit (over-length fees apply for surveys)
- 30% similarity threshold
- Direct submission (no pre-approval needed)
- Strong video/vision focus required

---

## REVISION CHECKLIST

### Critical (Before Submission)
- [ ] Fix duplicate labels (FeaturesDNN, ResNet)
- [ ] Add/fix neurochips figure reference
- [ ] Uncomment author information
- [ ] Fix math mode warning in feature_extraction.tex
- [ ] Fix 14 bibliography warnings
- [ ] Disable revision color markers

### High Priority
- [ ] Verify all NEW section citations
- [ ] Expand conclusion section
- [ ] Add summary comparison table

### Medium Priority
- [ ] Expand spiking networks section
- [ ] Update abstract coverage dates
- [ ] Address introduction objectives in conclusion

### Low Priority
- [ ] Check figure PDF compatibility
- [ ] Add resource utilization to all comparison tables
- [ ] Consider section rebalancing

---

## ESTIMATED EFFORT

| Task Category | Estimated Time |
|---------------|----------------|
| Critical LaTeX Fixes | 1-2 hours |
| Bibliography Cleanup | 2-3 hours |
| Conclusion Expansion | 2-3 hours |
| Spiking Networks Expansion | 4-6 hours |
| Citation Verification | 3-4 hours |
| Final Proofreading | 2-3 hours |
| **Total** | **14-21 hours** |

---

*Review generated: 2026-01-21*
