# Dataset Information

## Overview

The datasets used in this project were obtained following the Galaxy Training Network **Quality Control** tutorial.

The tutorial demonstrates quality control analysis of both:

- Single-end sequencing data
- Paired-end sequencing data

The analysis was performed using the Galaxy platform.

---

# 1. Dataset Used for FastQC Analysis

## Dataset Name

`female_oral2.fastq-4143.gz`

## Source

Zenodo

Dataset link:

https://zenodo.org/record/3977236/files/female_oral2.fastq-4143.gz

## Dataset Description

This dataset is a microbiome sequencing sample obtained from the oral microbiome of a snake.

The dataset was imported into Galaxy and renamed as:

`Reads`

## Sequencing Type

Single-end sequencing data.

## Analysis Performed

The dataset was analysed using FastQC to assess the quality of the sequencing reads.

The following FastQC quality metrics were examined:

- Basic Statistics
- Per Base Sequence Quality
- Per Sequence Quality Scores
- Per Base Sequence Content
- Per Sequence GC Content
- Sequence Duplication Levels
- Overrepresented Sequences
- Adapter Content

---

# 2. Datasets Used for MultiQC Analysis

## Dataset 1

`GSM461178_untreat_paired_subset_1.fastq`

## Dataset 2

`GSM461178_untreat_paired_subset_2.fastq`

## Source

Zenodo

Dataset links:

https://zenodo.org/record/61771/files/GSM461178_untreat_paired_subset_1.fastq

https://zenodo.org/record/61771/files/GSM461178_untreat_paired_subset_2.fastq

## Dataset Description

These datasets represent paired-end RNA-seq sequencing reads.

The two files represent reads generated from the same sequencing fragments:

- Dataset 1: Forward reads (Read 1)
- Dataset 2: Reverse reads (Read 2)

## Sequencing Type

Paired-end sequencing data.

---

# Data Processing

The paired-end datasets were processed using FastQC.

FastQC was run on both datasets simultaneously using the multiple dataset selection option in Galaxy.

The FastQC outputs were then combined using MultiQC.

MultiQC aggregated the FastQC quality metrics from both forward and reverse reads into a single report.

---

# Dataset Summary

| Analysis | Dataset | Sequencing Type | Tool Used |
|---|---|---|---|
| FastQC | female_oral2.fastq-4143.gz | Single-end | FastQC |
| MultiQC | GSM461178_untreat_paired_subset_1.fastq | Paired-end Read 1 | FastQC + MultiQC |
| MultiQC | GSM461178_untreat_paired_subset_2.fastq | Paired-end Read 2 | FastQC + MultiQC |

---

# Tutorial Source

The datasets and workflow were obtained from the Galaxy Training Network Quality Control tutorial.

Tutorial:

https://training.galaxyproject.org/training-material/topics/sequence-analysis/tutorials/quality-control/tutorial.html
