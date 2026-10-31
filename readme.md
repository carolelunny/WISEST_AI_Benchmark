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

## Why WISEST was developed
Systematic reviews are widely used to inform healthcare decisions, but reviews of similar questions can vary in methodological quality and risk of bias and can reach discordant conclusions. WISEST was developed to support transparent, consistent critical appraisal and to provide an expert reference for research on AI-assisted appraisal.

The project grew from earlier studies of discrepancies between systematic reviews, the reproducibility of the Jadad algorithm, and the challenges decision-makers face when choosing which review to trust. It has involved a large volunteer research community, including assessors recruited through Cochrane Engage, a crowdrecruiting site.

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

The 200-review study followed systematic-review guidance for identification and selection of source reviews, and adapted cross-sectional study reporting guidance. Eligible material included intervention and epidemiological systematic reviews, with or without meta-analysis and without publication-date or language restrictions. Overviews, scoping/evidence maps, methodological reviews, and reviews containing qualitative primary studies were excluded under that protocol. Its purpose was to compare appraisal constructs, responses, assessment time, and assessor agreement—not to estimate general-population benchmark performance.

The **600-review corpus** were assessed by two independent reviewers with senior-methodologist adjudication and ongoing extensive quality checking. 

## Annotation procedures
1. **Recruitment and expertise.** Volunteer assessors with systematic review methods experience were recruited using Cochrane Engage. 27 volunteers were recruited from September 2023 through April 2024.
2. **Training and piloting.** Assessors received training materials and a live or recorded walkthrough. They piloted at least three systematic review assessments, with senior-reviewer checking and feedback until their work followed the decision rules.
3. **Decision rules.** Structured interpretation rules were developed for AMSTAR 2 and ROBIS to reduce variation arising from broadly worded or multi-component items. 
4. **Source review assessment.** For each applicable item, the assessor recorded the judgement, a verbatim passage from the source review supporting it, and a written rationale. Review manuscripts, supplements, and available protocols were consulted.
5. **Evidence clarity.** Assessors recorded how clear or adequate the evidence was for the item-level judgement.
6. **Review characteristics.** Additional characteristics, including study eligibility information and methodological features, were extracted using structured guidance.

### Evidence clarity in the published study
| Published label | Meaning (paraphrased from the methods) |
|---|---|
| **Clear** | A direct quotation adequately supports a straightforward judgement. |
| **Weak** | Supporting material is vague, incomplete, difficult to interpret, or not directly quotable from the main review or supplementary material. |
| **Difference** | Contradictory passages in the source give conflicting information. |
| **No Information** | Relevant information is not found in the review, protocol, or supplementary materials. |

## Authorship, contributors and acknowledgements
**Project conception and scientific leadership:** **Carole Lunny, PhD**. 

**Human annotation and research contributions:** The WISEST corpus was developed with contributions from **30+ volunteer scientists** spanning evidence synthesis, clinical, and methodological research, recruited in part through **Cochrane Engage**. Contributions include source identification, appraisal, quotations and rationales, pilot assessment, quality checking, adjudication, data cleaning, analysis, and manuscript preparation. 

**Software and earlier subset:** The historical [WISEST-QA-Dataset](https://github.com/carolelunny/WISEST-QA-Dataset) repository preserves an earlier subset and software contributions. 

**Acknowledgement:** We thank the volunteer assessors, senior reviewers, quality checkers, students, and collaborators whose work made this research possible.

### Funding statement. 
Support from the University of Toronto’s Dalla Lana School of Public Health and the Temerity Centre for Artificial Intelligence Research and Education in Medicine was received through an AI for Population Health and Health Systems Implementation Grant (2023; $150,000). Funding from the University of Toronto Summer Undergraduate Data Science (SUDS) Opportunities Programme ($7,500) was received to hire a data science student to create code for the machine learning model in May 2023. We also received web support from nine students in the University of Toronto’s CSC301 Introduction to Software Engineering course (June–August 2023) to create a website to host our dataset and future WISEST AI tool to assess SRs using AMSTAR-2 and ROBIS. The Software Engineering course provides an internship project for students to support building websites such as our own. 

## Publications and related research
1. **Lunny C, Jain N, Nazari T, et al.** Exploring the methodological quality and risk of bias in 200 systematic reviews: A comparative study of ROBIS and AMSTAR-2 tools. *Research Synthesis Methods*. 2026;17:63–92. **https://doi.org/10.1017/rsm.2025.10032**  
   *Direct methods paper for the 200-review subset; includes study design, training, decision rules, quality checking, supplementary materials, and author contributions.*

2. **Lunny C, Whitelaw S, Reid EK, et al.** Exploring decision-makers' challenges and strategies when selecting multiple systematic reviews: insights for AI decision support tools in healthcare. *BMJ Open*. 2024;14:e084124. **https://doi.org/10.1136/bmjopen-2024-084124**  
   *Needs assessment of decision-makers and the proposed AI-assisted appraisal use case.*

3. **Lunny C, Thirugnanasampanthar SS, Kanji S, et al.** How can clinicians choose between conflicting and discordant systematic reviews? A replication study of the Jadad algorithm. *BMC Medical Research Methodology*. 2022;22:276. **https://doi.org/10.1186/s12874-022-01750-2**  
   *Demonstrates challenges in reproducibly selecting among conflicting systematic reviews.*

4. **Lunny C, Goodman I, Berrone S, et al.** When the Same Prompt Gives Different Answers (and the Same Answer Isn't Always Right): A Taxonomy of Failure Mechanisms, Testing, and Mitigation Strategies for LLM-Assisted Evidence Synthesis Read-and-Evaluate Tasks. arXiv:2610.39070. https://arxiv.org/abs/2610.39070

## How to cite WISEST
**If using methods or results from the published 200-review subset**, cite:
> Lunny C, Jain N, Nazari T, et al. Exploring the methodological quality and risk of bias in 200 systematic reviews: A comparative study of ROBIS and AMSTAR-2 tools. *Research Synthesis Methods*. 2026;17:63–92. https://doi.org/10.1017/rsm.2025.10032

**If referring to the expanded 600-review WISEST benchmark documentation**, cite this GitHub repository with its title, authorship/maintainer information, version or commit identifier, URL, and access date until a formal dataset citation or DOI is issued:
> Lunny C and the WISEST collaborators. *WISEST AI Benchmark: Expert-annotated benchmark for automated critical appraisal of systematic reviews* [repository documentation]. GitHub: https://github.com/carolelunny/WISEST_AI_benchmark. Version/commit: [insert]. Accessed: [insert date].

## Availability, licensing and responsible reuse
- **Public:** This README, references, and any documentation or clearly identified synthetic examples added to this repository.
- **Not publicly released here:** The 600-review corpus of annotations and verbatim source quotations.
- **Reuse:** Do not assume that the non-commercial licence intended for project-owned materials applies to third-party source articles, ROBIS/AMSTAR 2 instruments, or independently authored software. See `LICENSE.md` and any per-file rights statements once reviewed by the rights holders.

## Contact and updates
For questions about the benchmark, the expanded corpus, or permission to use non-public materials, contact the project lead through her public GitHub profile: **https://github.com/carolelunny**.
