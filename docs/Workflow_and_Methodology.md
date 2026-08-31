# Workflow and Methodology

## Overview

This project was completed as part of Week 2 of my NGS bioinformatics learning programme.

The objective was to understand the structure and quality assessment of FASTQ sequencing data and to perform quality control using FastQC and MultiQC.

The practical analysis was performed using the Galaxy platform following the Galaxy Training Network Quality Control tutorial.

---

# Analysis Workflow

```text
Sequencing datasets
        ↓
Import datasets into Galaxy
        ↓
Inspect FASTQ data
        ↓
Run FastQC
        ↓
Review individual quality metrics
        ↓
Run FastQC on paired-end datasets
        ↓
Aggregate FastQC results using MultiQC
        ↓
Interpret sequencing quality
