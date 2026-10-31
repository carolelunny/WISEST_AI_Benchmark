# WISEST — Which Systematic Evidence Synthesis is Best?
**An expert-annotated benchmark for evaluating automated critical appraisal of systematic reviews.**

**Project lead:** Carole Lunny, PhD  
**Project status:** 600-review annotation corpus assembled; expanded-corpus quality checks ongoing.  
**Public data status:** This repository documents the benchmark; the complete annotated 600-review corpus is **not** released here.

## At a glance
| Component | Current WISEST corpus |
|---|---:|
| Systematic reviews | 600 |
| Previously reported expert-labelled judgement count | 24,600 (pending reconciliation with the full instrument-level count) |
| ROBIS assessment entries | 26 per review: 21 signalling questions + 4 domain ratings + 1 overall rating |
| AMSTAR 2 items | 16 per review |
| Overall judgements | 2 per review across both tools (ROBIS overall included in 26 ROBIS entries; AMSTAR 2 overall additional) |
| Additional coded review characteristics | 33 per review |

Each labelled judgement is linked to **verbatim source evidence**, a **written rationale**, and an **evidence-clarity assessment**. The evidence-clarity categories are **Clear**, **Weak**, **Difference**, and **No Information**; see [Annotation procedures](#annotation-procedures) below.

> **Counting reconciliation needed:** The confirmed ROBIS count is 26 entries (21 signalling questions, four domain ratings, and one overall rating). Together with 16 AMSTAR 2 items and one separate AMSTAR 2 overall judgement, this implies **43 recorded ratings per review**, or **25,800 for 600 reviews**, if all fields are counted for every review. The previously reported **24,600** (41 per review) does not match this full field-level count. It remains a historical reported total pending verification of exactly which fields were included in that figure. Do not treat either total as a verified count of complete non-missing expert labels until reconciled against the actual data dictionary.

## Why WISEST was developed
Systematic reviews are widely used to inform healthcare decisions, but reviews of similar questions can vary in methodological quality and risk of bias and can reach discordant conclusions. WISEST was developed to support transparent, consistent critical appraisal and to provide an expert reference for research on AI-assisted appraisal.

The project grew from earlier studies of discrepancies between systematic reviews, the reproducibility of the Jadad algorithm, and the challenges decision-makers face when choosing which review to trust. It has involved a large volunteer research community, including assessors recruited through Cochrane Engage.

A companion methodological study applied ROBIS and AMSTAR 2 to **200 systematic reviews** and examined the overlap between the tools, item and overall ratings, assessment time, and agreement between assessors. That published analysis is a **subset study**, not a validation report for all 600 reviews.

## Intended applications
WISEST can support studies of:
- Accuracy of automated ROBIS and AMSTAR 2 judgements against expert assessments.
- Whether a model's explanation and cited source evidence support its judgement.
- Reliability and repeatability under repeated model runs or changes to evaluation conditions.
- Differences between item-level results and overall assessments.
- Sensitivity to source-evidence clarity, ambiguity, and contradictory text.

**Scope limitation:** WISEST is a benchmark for critical appraisal of research evidence. It is **not** itself a frontier-AI safety or biosecurity benchmark. Its annotation and verification methods may inform research on reliability of AI evaluators, but transfer to safety-specific domains requires separate testing.

## Study protocol and design
The protocol for the published methodological comparison of **200 reviews** was registered on the Open Science Framework:
**[Open Science Framework: WISEST study materials and protocol](https://osf.io/nbcta/)**

The 200-review study followed systematic-review guidance for identification and selection of source reviews, and adapted cross-sectional study reporting guidance. Eligible material included intervention and epidemiological systematic reviews, with or without meta-analysis and without publication-date or language restrictions. Overviews, scoping/evidence maps, methodological reviews, and reviews containing qualitative primary studies were excluded under that protocol.

The published sample comprised 139 reviews drawn from an AMSTAR 2 methodological study, 34 from a ROBIS methodological study, and 27 additional reviews from the Cochrane Database of Systematic Reviews. Its purpose was to compare appraisal constructs, responses, assessment time, and assessor agreement—not to estimate general-population benchmark performance.

For the **expanded 600-review corpus**, the project summary reports two independent review assessments with senior-methodologist adjudication and ongoing extensive quality checking. The final expanded-corpus protocol, item dictionary, selection process, and quality-control summary should be published separately or linked here once finalized. The 200-review protocol must not be presented as if it fully describes every aspect of the expanded corpus.

## Annotation procedures
The published 200-review methods study describes the following process:
1. **Recruitment and expertise.** Volunteer assessors with systematic-review methods experience were recruited using Cochrane Engage; the paper reports 27 volunteers recruited from September 2023 through April 2024.
2. **Training and piloting.** Assessors received training materials and a live or recorded walkthrough. They piloted at least three systematic-review assessments, with senior-reviewer checking and feedback until their work followed the decision rules.
3. **Decision rules.** Structured interpretation rules were developed for AMSTAR 2 and ROBIS to reduce variation arising from broadly worded or multi-component items. See the published study's Supplementary Appendix C.
4. **Source review assessment.** For each applicable item, the assessor recorded the judgement, a verbatim passage from the source review supporting it, and a written rationale. Review manuscripts, supplements, and available protocols were consulted.
5. **Evidence clarity.** Assessors recorded how clear or adequate the evidence was for the item-level judgement.
6. **Review characteristics.** Additional characteristics, including study eligibility information and methodological features, were extracted using structured guidance. See Supplementary Appendix D for the 200-review study's extraction elements.

### Evidence clarity in the published study
| Published label | Meaning (paraphrased from the methods) |
|---|---|
| **Clear** | A direct quotation adequately supports a straightforward judgement. |
| **Weak** | Supporting material is vague, incomplete, difficult to interpret, or not directly quotable from the main review or supplementary material. |
| **Difference** | Contradictory passages in the source give conflicting information. |
| **No Information** | Relevant information is not found in the review, protocol, or supplementary materials. |

These four labels should be used consistently in the public data dictionary. The codebook should explain their operational definitions, particularly the distinction between **Weak** and **No Information**.

## Quality checking and adjudication
**Published 200-review study:** Initial pilot assessments were checked by senior reviewers. After training, random checks were used for quality assurance. Seven volunteer assessors were promoted to quality-checker roles. The paper reports that **168 of 200 reviews (84%)** received senior-assessor quality checking. Item agreement was also compared with assessments from earlier published studies where applicable.

**Expanded 600-review project:** The current project summary states that each review has been independently assessed by two reviewers and adjudicated by a senior methodologist, with extensive quality checking still underway. This status should be updated when the expanded protocol and dataset quality-control report are finalized.

These are different descriptions of distinct study stages. **The published 84% checking result should not be represented as the final checking or adjudication statistic for all 600 reviews.**

## Authorship, contributors and acknowledgements
**Project conception and scientific leadership:** **Carole Lunny, PhD**. The published 200-review study specifies that Carole Lunny conceived and designed that study.

**Human annotation and research contributions:** The WISEST corpus has been developed with contributions from **30+ volunteer scientists** spanning evidence synthesis, clinical, and methodological research, recruited in part through **Cochrane Engage**. Contributions include source identification, appraisal, quotations and rationales, pilot assessment, quality checking, adjudication, data cleaning, analysis, and manuscript preparation. The detailed contributor roles for the published 200-review study are provided in the paper's **Author contributions** section and should be used rather than assigning unverified roles to named individuals here.

**Software and earlier subset:** The historical [WISEST-QA-Dataset](https://github.com/carolelunny/WISEST-QA-Dataset) repository preserves an earlier subset and software contributions. Its upstream authors and commit history should be credited independently from the scientific leadership of the expanded benchmark.

**Acknowledgement:** We thank the volunteer assessors, senior reviewers, quality checkers, students, and collaborators whose work made this research possible. See the published article for the full author list and specific author contributions.

### Funding context
The expanded annotation work has relied heavily on volunteer contributions. The published **200-review methods study** also reports institutional and student-program support for associated AI, coding, and website work (see its Funding statement). Therefore, it would be inaccurate to describe **all components of WISEST** as having received no funding.

## Publications and related research
1. **Lunny C, Jain N, Nazari T, et al.** Exploring the methodological quality and risk of bias in 200 systematic reviews: A comparative study of ROBIS and AMSTAR-2 tools. *Research Synthesis Methods*. 2026;17:63–92. **https://doi.org/10.1017/rsm.2025.10032**  
   *Direct methods paper for the 200-review subset; includes study design, training, decision rules, quality checking, supplementary materials, and author contributions.*

2. **Lunny C, Whitelaw S, Reid EK, et al.** Exploring decision-makers' challenges and strategies when selecting multiple systematic reviews: insights for AI decision support tools in healthcare. *BMJ Open*. 2024;14:e084124. **https://doi.org/10.1136/bmjopen-2024-084124**  
   *Needs assessment of decision-makers and the proposed AI-assisted appraisal use case.*

3. **Lunny C, Thirugnanasampanthar SS, Kanji S, et al.** How can clinicians choose between conflicting and discordant systematic reviews? A replication study of the Jadad algorithm. *BMC Medical Research Methodology*. 2022;22:276. **https://doi.org/10.1186/s12874-022-01750-2**  
   *Demonstrates challenges in reproducibly selecting among conflicting systematic reviews.*

Further manuscripts about the expanded WISEST corpus, automated evaluation, or the FAILS taxonomy should be linked here **when publicly available**; planned work is not listed as published.

## How to cite WISEST
**If using methods or results from the published 200-review subset**, cite:
> Lunny C, Jain N, Nazari T, et al. Exploring the methodological quality and risk of bias in 200 systematic reviews: A comparative study of ROBIS and AMSTAR-2 tools. *Research Synthesis Methods*. 2026;17:63–92. https://doi.org/10.1017/rsm.2025.10032

**If referring to the expanded 600-review WISEST benchmark documentation**, cite this GitHub repository with its title, authorship/maintainer information, version or commit identifier, URL, and access date until a formal dataset citation or DOI is issued:

> Lunny C and the WISEST collaborators. *WISEST: Expert-annotated benchmark for automated critical appraisal of systematic reviews* [repository documentation]. GitHub: https://github.com/carolelunny/WISEST-benchmark. Version/commit: [insert]. Accessed: [insert date].

The expanded dataset should receive its **own formal data citation and version/DOI** if and when a distributable release is published. Do not treat the 200-review paper as a complete citation for 600 records.

## Availability, licensing and responsible reuse
- **Public:** This README, references, and any documentation or clearly identified synthetic examples added to this repository.
- **Not publicly released here:** The complete 600-review annotations and verbatim source quotations.
- **Reuse:** Do not assume that the non-commercial licence intended for project-owned materials applies to third-party source articles, ROBIS/AMSTAR 2 instruments, or independently authored software. See `LICENSE.md` and any per-file rights statements once reviewed by the rights holders.
- **Evaluation integrity:** Public release of item-level expert labels could compromise future held-out evaluation. A future release should distinguish development, evaluation, and restricted test sets.

## Contact and updates
For questions about the benchmark, the expanded corpus, or permission to use non-public materials, contact the project lead through her public GitHub profile: **https://github.com/carolelunny**.

**Items to confirm before final publication:** reconcile the previously reported 24,600 judgements with the 43-field instrument count; verify missingness and which ratings are included in the released dataset; expanded-corpus selection and adjudication protocol; detailed evidence-clarity codebook; contributor role and attribution list; public-release/access process; and rights/licensing for each material type.