# What Makes an NGS Sample Pass or Fail?

## Overview

NGS sequencing data should be assessed using multiple quality control metrics before proceeding to downstream analysis. A sample does not necessarily fail because of one warning; the overall QC profile and the severity of the issue should be considered.

---

## NGS QC Pass/Fail Criteria

| QC Metric | PASS | REVIEW / WARNING | FAIL |
|---|---|---|---|
| **Per Base Sequence Quality** | Quality scores remain high across most positions, generally above Q20–Q30. | Quality decreases towards the end of reads but most bases remain usable. | A substantial proportion of bases have consistently low quality scores. |
| **Per Sequence Quality Scores** | Most reads have high average quality scores. | A noticeable proportion of reads have lower average quality. | A large proportion of reads have consistently low average quality. |
| **Per Base Sequence Content** | Base composition is relatively consistent or expected for the library type. | Moderate variation is observed and may be explained by library preparation or sequencing bias. | Strong unexplained bias is observed across the reads. |
| **Per Sequence GC Content** | GC distribution is consistent with the expected sample or organism. | Some deviation from the expected distribution is observed. | Major unexplained deviation or multiple abnormal peaks suggest possible contamination. |
| **Sequence Duplication Levels** | Duplication is consistent with the expected library type and sequencing depth. | Elevated duplication requires investigation. | Extremely high duplication suggests substantial PCR bias or low library complexity. |
| **Adapter Content** | No significant adapter contamination is detected. | Low or moderate adapter contamination is present and trimming may be required. | High adapter contamination is present and reads require adapter trimming before downstream analysis. |

---

## Important Principle

A FastQC **warning or failure does not automatically mean that an NGS sample must be discarded**.

The result should be interpreted by considering:

- The sequencing experiment type
- Library preparation method
- Expected GC content
- Read quality across the sequencing length
- Level of duplication
- Presence of adapter contamination
- Whether the problem can be corrected through trimming or filtering

---

# QC Decision for the Analysed Samples

The samples assessed were:

- Paired_R1
- Paired_R2

## QC Results

| QC Metric | Paired_R1 | Paired_R2 | Decision |
|---|---|---|---|
| Per Base Sequence Quality | Good overall | Good overall | PASS |
| Per Sequence Quality Scores | High quality | High quality | PASS |
| Per Base Sequence Content | Variable | Variable | REVIEW |
| Per Sequence GC Content | Consistent | Consistent | PASS |
| Sequence Duplication Levels | Acceptable | Acceptable | PASS |
| Adapter Content | No substantial contamination detected | No substantial contamination detected | PASS |

---

# Final Pass/Fail Decision

## Paired_R1: PASS WITH REVIEW

The sample shows generally high sequencing quality and no substantial adapter contamination. However, variation in base sequence content should be documented and considered during downstream analysis.

## Paired_R2: PASS WITH REVIEW

The sample shows generally high sequencing quality and no substantial adapter contamination. Variation in base sequence content should also be reviewed during downstream analysis.

---

# Overall Conclusion

Both samples are considered suitable for downstream analysis.

The samples are classified as:

**PASS WITH REVIEW**

The QC results do not indicate that the sequencing data should be discarded. However, the observed variation in per-base sequence content and any decline in quality towards the ends of reads should be considered during subsequent quality trimming and analysis.

---

## Recommended Next Steps

Before downstream analysis:

1. Review the FastQC and MultiQC reports.
2. Perform quality trimming if low-quality read ends are present.
3. Remove adapter sequences if detected.
4. Run FastQC and MultiQC again after trimming.
5. Compare pre-trimming and post-trimming QC results before proceeding with downstream analysis.
