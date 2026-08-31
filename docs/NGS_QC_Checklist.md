# NGS QC Checklist

## Week 2: NGS Quality Control

This checklist summarises the quality control assessment performed using **FastQC** and **MultiQC** for the paired-end sequencing samples:

- Paired_R1
- Paired_R2

---

## Six-Metric QC Interpretation Table

| QC Metric | What was checked? | Result | Interpretation |
|---|---|---|---|
| **Per Base Sequence Quality** | Quality scores across each base position | Quality was high across most read positions. A decline was observed towards the end of the reads, particularly in later positions. | Overall sequencing quality is good, although the decline in quality towards the read ends should be considered during downstream processing. |
| **Per Sequence Quality Scores** | Distribution of average quality scores across all reads | Most reads were concentrated in the high-quality range, with mean sequence quality predominantly above Q30. | The majority of reads have good overall sequencing quality and are suitable for downstream analysis. |
| **Per Base Sequence Content** | Distribution of A, T, G and C across read positions | Base composition varied across positions, particularly at the beginning of the reads. | This variation may indicate sequence composition or library preparation bias and should be documented for downstream analysis. |
| **Per Sequence GC Content** | Distribution of GC percentage across all reads | Both samples showed a similar GC distribution, with the main peak occurring at approximately 55–58% GC. | The GC distributions are consistent between the paired samples. |
| **Sequence Duplication Levels** | Frequency of duplicated sequences | Most sequences occurred at low duplication levels, with duplication decreasing substantially at higher levels. | Overall duplication levels appear acceptable for these samples. |
| **Adapter Content** | Presence of known adapter sequences within reads | MultiQC reported that adapter contamination was below 0.1% for hidden sample-adapter combinations. | No substantial adapter contamination was detected in Paired_R1 and Paired_R2. |

---

## QC Summary

| Sample | Overall QC Assessment |
|---|---|
| **Paired_R1** | PASS WITH REVIEW |
| **Paired_R2** | PASS WITH REVIEW |

### Overall Interpretation

The MultiQC assessment indicates that both paired-end sequencing samples have generally good sequencing quality. The majority of reads show high mean quality scores, the GC distributions are similar between samples, and no substantial adapter contamination was detected.

However, variation in per-base sequence content and a reduction in sequencing quality towards the ends of some reads should be considered during downstream processing.

**Overall decision: Both samples are suitable for further downstream analysis, with QC observations documented for review.**

---

## Evidence

The QC assessment was performed using:

- FastQC
- MultiQC

The evidence includes:

- Basic Statistics
- Per Base Sequence Quality
- Per Sequence Quality Scores
- Per Base Sequence Content
- Per Sequence GC Content
- Sequence Duplication Levels
- Adapter Content
- Sequence Counts

Detailed FastQC and MultiQC reports and associated plots are available in the `evidence/` folder.

---

## Tools Used

- FastQC
- MultiQC
