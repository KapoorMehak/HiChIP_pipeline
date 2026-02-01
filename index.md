# HiChIP_pipeline
HiChIP Working Methodology
## Objective
Identify enhancer–promoter interactions using HiChIP.

This document describes a **step-by-step working methodology** for processing HiChIP data, starting from raw FASTQ files through alignment, quality control, contact matrix generation, loop calling, and visualization.

The pipeline is implemented using the **Dovetail Genomics HiChIP workflow**, combined with standard Hi-C and ChIP-seq analysis tools.

---

## Pipeline overview
**Main steps**
1. Pre-alignment and reference preparation  
2. Alignment and valid pair generation  
3. Library quality control  
4. Contact matrix generation  
5. Loop calling  
6. Visualization and interpretation  

---
## Sections
- [Prerequisites](prerequisites.md)
- [Input files](input_files.md)
- [Pre-alignment](prealignment.md)
- [Alignment and valid pairs](alignment_valid_pairs.md)
- [Library QC](qc.md)
- [Contact matrix generation](contact_matrix.md)
- [Loop calling](loop_calling.md)
- [Visualization](visualization.md)
- [References](references.md)
