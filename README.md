# Week 2 — NGS Foundations, FASTQ Quality Control and MultiQC

## Project Overview

This repository documents my Week 2 practical work on Next-Generation Sequencing (NGS) quality control.

The project focuses on understanding FASTQ files, Phred quality scores, sequencing quality metrics, and the use of FastQC and MultiQC for assessing sequencing read quality.

The practical analysis was performed using the Galaxy platform following the Galaxy Training Network Quality Control tutorial.

---

## Learning Objectives

During this project, I learned about:

- FASTQ file structure
- Phred quality scores
- Single-end and paired-end sequencing data
- Per-base sequence quality
- Per-sequence quality scores
- GC content
- Sequence duplication levels
- Adapter content
- Overrepresented sequences
- FastQC quality reports
- MultiQC report aggregation

---

## Dataset Information

The datasets used for this practical exercise were obtained through the Galaxy Training Network Quality Control tutorial.

The datasets were downloaded/imported into Galaxy and used for quality control analysis.

Detailed information about the datasets is available in:

[Dataset Information](docs/Dataset_Information.md)

---

## Workflow

The analysis workflow followed was:

FASTQ datasets
        ↓
Upload / Import into Galaxy
        ↓
FastQC
        ↓
Individual quality assessment
        ↓
MultiQC
        ↓
Combined quality assessment and report generation
        ↓
Interpretation of QC metrics

Detailed methodology is available in:

[Workflow and Methodology](docs/Workflow_and_Methodology.md)

---

## Tools Used

- Galaxy
- FastQC
- MultiQC

---

## Key Quality Metrics Examined

The following quality control metrics were examined:

1. Basic sequence statistics
2. Per-base sequence quality
3. Per-sequence quality scores
4. Per-sequence GC content
5. Sequence duplication levels
6. Adapter content
7. Overrepresented sequences
8. Per-base sequence content

---

## Repository Structure

```text
docs/
    Dataset_Information.md
    Workflow_and_Methodology.md
    NGS_QC_Checklist.md
    What_Makes_an_NGS_Sample_Pass_or_Fail.md

evidence/
    fastqc/
    multiqc/
