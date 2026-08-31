# NGS QC Checklist

## Week 2: NGS Quality Control

This checklist summarises the quality control assessment performed using FastQC.

## QC Observation Table

| QC Metric | What I Observed | What It Means |
|---|---|---|
| **Per-base quality** | Quality is very high at the beginning of the reads (around Q37–38), but it drops sharply after ~100 bp. Toward the 3′ end, the median quality falls to around Q12–18, with a wide spread of quality scores. | **Sequencing quality decreases substantially toward the end of the reads.** The later bases are less reliable and may need quality trimming before downstream analysis. |
| **Per-sequence quality** | The distribution is unusual/bimodal, with a large peak around **Phred Q21** and another peak around **Q36–37**. | The reads do not have one consistent overall quality level. A substantial group of reads has relatively low mean quality (~Q21), while another group has high quality. This explains the FastQC warning and suggests that some reads may need further QC. |
| **GC content** | Overall GC content is **44%**. The observed GC distribution is not a smooth single peak and differs noticeably from the theoretical distribution, with several peaks around approximately **39%, 43%, and 51%**. | The GC composition is **non-uniform and deviates from the expected distribution**. This can indicate sequence composition bias, a mixture of different sequence populations, contamination, or other library/sample characteristics. It requires further investigation rather than automatically meaning contamination. |
| **Duplication** | FastQC reports **36.82% of sequences remaining after deduplication**, meaning approximately **63.18% of sequences are duplicates**. There is a particularly large group of sequences occurring at duplication level >10. | The dataset has a **high level of sequence duplication**. This may indicate PCR amplification bias, over-sequencing, or genuinely abundant sequences, depending on the type of experiment. |
| **Adapter content** | Adapter sequences are detected at high levels. The graph shows approximately **54% Nextera Transposase sequence** and **47% Illumina Small RNA 3′ adapter sequence** toward the later read positions. | There is **substantial adapter contamination/presence**, especially toward the later part of the reads. Adapter trimming should be considered before downstream analysis. |
| **Overrepresented sequences** | FastQC identifies several highly abundant sequences. The most frequent sequence occurs **46 times (~5.67%)**, followed by sequences at ~5.05%, ~4.80%, and ~4.06%. FastQC reports **"No Hit"** for their possible source. | Certain sequences occur much more frequently than expected. Because FastQC could not identify their source, we **cannot conclude from this report alone** whether they are adapters, biological sequences, or contamination. Their identity should be investigated further. |

## Evidence

The FastQC and MultiQC evidence is available in the `evidence` folder.

The evidence includes:

- Basic Statistics
- Per Base Sequence Quality
- Per Sequence Quality Scores
- GC Content
- Sequence Duplication Levels
- Adapter Content
- Overrepresented Sequences
- Per Base Sequence Content
- MultiQC Report
