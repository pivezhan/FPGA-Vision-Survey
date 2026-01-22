# FPGA Vision Survey - Revision Session Log

This file tracks revision sessions for the FPGA Vision Accelerators Survey.

---

## Survey Status Summary

| Metric | Value |
|--------|-------|
| Total Papers Covered | 102 |
| Coverage Period | 2013-2025 |
| Total LaTeX Lines | ~1,229 |
| Figures | 67 |
| Bibliography Entries | 211+ |
| NEW Content Markers | 259 (`\rev{}`) |
| Grammatical Revisions | 100+ (`\revb{}`) |

---

## Session Log

### Session 1 - 2026-01-21

**Objectives:**
- Initialize Claude Code documentation (CLAUDE.md)
- Create revision tracking (SESSION_LOG.md)
- Identify target venues for submission

**Completed:**
- [x] Created CLAUDE.md with build instructions and survey overview
- [x] Created SESSION_LOG.md for tracking revisions
- [x] Research target conferences/journals (see detailed analysis below)

**Survey State:**
- Current format: IEEE conference (`IEEEtran.cls`)
- Revision markers active (colors enabled)
- NEW sections added: Vision Transformers, Edge AI

**Next Steps:**
- [ ] Identify best matching conference/journal for submission
- [ ] Review and update bibliography (2024-2025 papers)
- [ ] Finalize revision markers
- [ ] Prepare submission-ready version

---

## Revision Checklist

### Content Review
- [ ] Abstract - verify claims and coverage
- [ ] Introduction - update with recent context
- [ ] Feature Extraction - check for recent methods
- [ ] Neural Networks (739 lines) - comprehensive review needed
- [ ] Vision Transformers (NEW) - ensure completeness
- [ ] Edge AI (NEW) - verify recent implementations
- [ ] Spiking Networks - expand if needed
- [ ] Conclusion - align with updated content

### Technical Review
- [ ] Verify all citations resolve correctly
- [ ] Check figure quality and captions
- [ ] Validate comparison tables
- [ ] Confirm metric calculations

### Format Review
- [ ] Match target venue style
- [ ] Check page/word limits
- [ ] Verify author information
- [ ] Prepare supplementary materials if needed

---

## Target Venues - Detailed Analysis

### TIER 1: BEST MATCH JOURNALS (Recommended)

#### 1. ACM Transactions on Reconfigurable Technology and Systems (TRETS) ⭐ TOP PICK
- **Scope**: Premier archival journal for reconfigurable computing (FPGAs)
- **Survey Policy**: Contact Editor-in-Chief before submission with proposed topic and outline
- **Recent Survey Example**: "A Survey of FPGA-based Neural Network Inference Accelerators" (199 citations, 3,400+ downloads)
- **Fit Score**: 95% - Directly aligned with FPGA + vision accelerators
- **URL**: https://dl.acm.org/journal/trets
- **Note**: Survey papers require pre-approval from EiC

#### 2. IEEE Transactions on Circuits and Systems for Video Technology (TCSVT)
- **Impact Factor**: Q1 journal
- **Scope**: Circuits and systems for video technologies, hardware implementations
- **Survey Policy**: "Original review articles and surveys are acceptable"
- **Page Limit**: 14 pages (2-column IEEE format); over-length charges after 14 pages for surveys
- **Similarity Check**: Max 30% (original) or 50% (expanded)
- **Submission**: https://mc.manuscriptcentral.com/tcsvt
- **Fit Score**: 85% - Strong match for vision + hardware focus

#### 3. ACM Computing Surveys (CSUR)
- **Status**: Premier survey venue across all CS
- **Scope**: Comprehensive surveys and tutorial papers
- **Submission**: https://mc.manuscriptcentral.com/csur
- **Rejection Policy**: 12-month resubmission ban after rejection
- **Fit Score**: 75% - General venue, less FPGA-specific

#### 4. IEEE Access
- **Impact Factor**: 3.6 (Q1)
- **Article Processing Charge**: $1,995 USD (waivers available)
- **Turnaround**: 4-6 weeks submission to publication
- **Review Process**: Binary accept/reject (no revisions)
- **Scope**: Welcomes review/survey papers
- **Fit Score**: 70% - Fast open-access option

### TIER 2: FPGA-FOCUSED CONFERENCES

#### 1. ISFPGA 2026 (ACM/SIGDA International Symposium on FPGAs)
- **Date**: TBD, 2026
- **Location**: Seaside, California, USA
- **Status**: Premier FPGA conference
- **CFP**: https://www.isfpga.org/call-for-papers/
- **Fit Score**: 80% - Top venue but primarily original research

#### 2. FCCM 2026 (IEEE Field-Programmable Custom Computing Machines)
- **Date**: TBD, 2026
- **Status**: Original and premier FPGA forum
- **CFP**: https://www.fccm.org/
- **Fit Score**: 75% - Excellent for FPGA work

#### 3. FPL 2026 (Field-Programmable Logic and Applications)
- **Date**: September 7-11, 2026
- **Location**: Ghent University, Belgium
- **Status**: Largest FPL conference (36th edition)
- **Topics**: Architectures, Tools, Applications, HPC, Security
- **URL**: https://fpl.org/
- **Fit Score**: 75% - Broad FPL audience

### TIER 3: ALTERNATIVE OPTIONS

#### Frontiers in High Performance Computing
- **Recent FPGA Survey**: "FPGA innovation research in the Netherlands" (2025)
- **Scope**: FPGA architecture, HPC, programming models
- **Fit Score**: 65% - Newer venue, less established

#### MDPI Electronics / Applied Sciences
- **Type**: Open access
- **Special Issues**: FPGA-focused issues available
- **Fit Score**: 60% - Fast publication, lower prestige

---

## RECOMMENDATION SUMMARY

| Rank | Venue | Type | Fit | Notes |
|------|-------|------|-----|-------|
| 1 | **ACM TRETS** | Journal | 95% | Contact EiC first; best FPGA match |
| 2 | **IEEE TCSVT** | Journal | 85% | Direct submission; vision focus |
| 3 | **IEEE Access** | Journal | 70% | Fast OA; lower prestige |
| 4 | **FPL 2026** | Conference | 75% | Sept 2026; broad audience |
| 5 | **ISFPGA 2026** | Conference | 80% | Premier venue; original research |

**Primary Recommendation**: Submit to **ACM TRETS** after contacting the Editor-in-Chief with a brief outline. This is the most prestigious and directly relevant venue for FPGA accelerator surveys.

**Backup Option**: **IEEE TCSVT** accepts surveys directly and has strong alignment with vision + hardware topics.

---

## Notes

### Strengths of This Survey
- Comprehensive coverage (102 papers, 2013-2025)
- NEW sections on Vision Transformers and Edge AI
- Detailed 23-metric comparison framework
- Covers emerging FPGA platforms (Agilex, Versal)

### Areas for Enhancement
- Expand neuromorphic/SNN section
- Add more 2024-2025 papers
- Include hardware-aware NAS discussion
- Consider adding reproducibility/open-source tools section

---

*Last Updated: 2026-01-21*
