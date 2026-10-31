# WISEST data dictionary
WISEST (*Which Systematic Evidence Synthesis is Best?*) contains systematic review characteristics and human assessments using **ROBIS** and **AMSTAR 2**, with supporting quotations, rationales, and evidence-clarity annotations. The expanded corpus comprises 600 reviews. 

## How to read this dictionary
- **Assessment item:** an answer to a tool's signalling question or AMSTAR 2 item.
- **Domain judgement:** a combined synthesis rating based on a tool domain, not another signalling question.
- **Final-stage overall judgement:** an additional question that informs ROBIS overall judgement; report separately from the 21 ROBIS domain signalling questions.
- **Characteristic:** descriptive information about a systematic review (e.g., year of publication).
- **Supporting material:** quotation, rationale, clarification, or notes.

## 1. Record identifiers and bibliographic fields
| Field (human-readable alias) | Source heading / description | Type / expected content | Notes |
|---|---|---|---|
| `review_id` | ID# | Unique identifier | Appears in more than one worksheet/section; verify join key |
| `reviewer_initials` | Reviewer initials; Reviewer Name/Initials | Text | May identify assessment or characteristic coder; do not automatically publish identities |
| `first_author_year` | First Author Year | Text | Bibliographic shorthand |
| `title` | Title; Article title | Text | May be duplicated across tabs |
| `objective` | Objective | Text | Review question/objective |
| `primary_intervention_or_exposure` | Primary Intervention OR exposure | Text | As recorded |
| `primary_outcome` | Primary outcome | Text | As recorded |
| `main_abstract_finding` | Main finding from the abstract | Text | Descriptive extraction |
| `doi_or_pmid` | DOI or PMID | Identifier | Could contain either kind of identifier |
| `full_text_location` | Link to free full text ... OR PDF already uploaded in Google Drive | URL / document pointer | May point to restricted files; screen before release |
| `publication_year` | Publication Year | Year | Source also contains year in `first_author_year` |

## 2. ROBIS assessment
The workbook visibly lists **21 domain signalling questions**, **four domain concern judgements**, **three additional final-stage questions (A–C)**, and **one overall ROBIS judgement**. The doamin and overall judgments are `low`, `high`, `unclear` tisk of bias for the overall ratings. 

### Domain 1 — Study eligibility criteria
| Code | Signalling question (from the workbook; lightly standardized punctuation) |
|---|---|
| ROBIS 1.1 | Did the review adhere to pre-defined objectives and eligibility criteria? |
| ROBIS 1.2 | Were the eligibility criteria appropriate for the review question? |
| ROBIS 1.3 | Were eligibility criteria unambiguous? |
| ROBIS 1.4 | Were restrictions based on study characteristics appropriate (e.g., date, sample size, study quality, outcomes)? Record the characteristic where relevant. |
| ROBIS 1.5 | Were restrictions based on sources of information appropriate (e.g., publication status/format, language, data availability)? |
| Domain 1 judgement | Concerns regarding specification of eligibility criteria: **low / high / unclear** |

### Domain 2 — Identification and selection of studies
| Code | Signalling question |
|---|---|
| ROBIS 2.1 | Did the search include an appropriate range of databases/electronic sources for published and unpublished reports? |
| ROBIS 2.2 | Were additional methods beyond database searching used to identify reports? |
| ROBIS 2.3 | Were the search terms and structure likely to retrieve as many eligible studies as possible? |
| ROBIS 2.4 | Were date, publication-format, or language restrictions appropriate? |
| ROBIS 2.5 | Were efforts made to minimise errors in study selection? |
| Domain 2 judgement | Concerns regarding identification and selection: **low / high / unclear** |

### Domain 3 — Data collection and study appraisal
| Code | Signalling question |
|---|---|
| ROBIS 3.1 | Were efforts made to minimise errors in data collection? |
| ROBIS 3.2 | Were sufficient study characteristics considered to interpret the results? |
| ROBIS 3.3 | Were all relevant study results collected for synthesis? |
| ROBIS 3.4 | Was risk of bias or methodological quality assessed with appropriate criteria? |
| ROBIS 3.5 | Were efforts made to minimise errors in risk-of-bias assessment? |
| Domain 3 judgement | Concerns regarding data collection and appraisal: **low / high / unclear** |

### Domain 4 — Synthesis and findings
| Code | Signalling question |
|---|---|
| ROBIS 4.1 | Did the synthesis include all studies that it should? |
| ROBIS 4.2 | Were all predefined analyses reported, or departures explained? |
| ROBIS 4.3 | Was the synthesis appropriate for the questions, designs, and outcomes? |
| ROBIS 4.4 | Was heterogeneity minimal or adequately addressed? |
| ROBIS 4.5 | Were findings robust, e.g., by funnel plot or sensitivity analysis? |
| ROBIS 4.6 | Were biases in primary studies minimal or addressed in the synthesis? |
| Domain 4 judgement | Concerns regarding synthesis and findings: **low / high / unclear** |

### Final-stage supporting questions and overall judgement
| Code | Field |
|---|---|
| ROBIS A | Did interpretation address concerns identified in Domains 1–4? |
| ROBIS B | Was the relevance of identified studies to the review question appropriately considered? |
| ROBIS C | Did reviewers avoid emphasizing results based on statistical significance? |
| ROBIS overall judgment | Overall risk-of-bias judgement: **low / high / unclear risk of bias** |

## 3. AMSTAR 2 assessment
Sixteen numbered AMSTAR 2 items.

| Code | AMSTAR 2 item / spreadsheet field |
|---|---|
| 1 | Do the review questions and inclusion criteria include PICO components? |
| 2 | Was a protocol established before the review and were important deviations justified? |
| 3 | Did authors explain their choice of study designs? |
| 4 | Did authors use a comprehensive literature search strategy? |
| 5 | Was study selection performed in duplicate? |
| 6 | Was data extraction performed in duplicate? |
| 7 | Was a list of excluded studies provided with justifications? |
| 8 | Were included studies described adequately? |
| 9 | Was risk of bias of individual included studies assessed satisfactorily? |
| 10 | Were funding sources of included studies reported? |
| 11 | If meta-analysis was performed, were synthesis methods appropriate? |
| 12 | If meta-analysis was performed, did authors assess the impact of risk of bias on results? |
| 13 | Did authors account for study risk of bias when interpreting/discussing results? |
| 14 | Was heterogeneity adequately explained and discussed? |
| 15 | If quantitative synthesis was performed, was publication/small-study bias investigated and its impact discussed? |
| 16 | Were review-level conflicts of interest and funding disclosed? |
| AMSTAR 2 overall | Overall quality: **High / Moderate / Low / Critically low quality** |

## 4. Review-characteristics worksheet
**30 coded characteristics per review**

| No. | Field | Description / likely representation |
|---|---|---|
| 1 | Article title | Text |
| 2 | Abstract | Text |
| 3 | Journal name | Full journal name |
| 4 | Language | Language of the review |
| 5 | Number of authors | Integer |
| 6 | Country | Country of first-author affiliation |
| 7 | Topic | Disease/topic classified using ICD-10 |
| 8 | Sub-topic | ICD-10 subtopic |
| 9 | Care setting | As reported (e.g., inpatient/outpatient, rural/urban) |
| 10 | Protocol presence | Whether a protocol was reported |
| 11 | Population eligibility | Inclusion and exclusion details |
| 12 | Intervention/exposure eligibility | Inclusion and exclusion details |
| 13 | Comparator eligibility | Inclusion and exclusion details |
| 14 | Outcome eligibility | Including timing and effect measures |
| 15 | Number of included primary studies | Integer where known |
| 16 | Meta-analysis or network meta-analysis | Whether MA/NMA was conducted |
| 17 | Review type | Review design/type |
| 18 | Included primary-study designs | Check consistency with AMSTAR 2 item 3 |
| 19 | Review ranking | Workbook ranks NMA RCT/IPD, pairwise RCT, observational MA/NMA, narrative and other review types; verify exact codes and ties |
| 20 | Matching review | Workbook instruction **LEAVE BLANK**; do not assume populated |
| 21 | Cochrane review | Yes/No based on source |
| 22 | Equity focus | Whether PROGRESS-Plus dimensions were addressed |
| 23 | Conflict-of-interest disclosure | Whether declared |
| 24 | Funding source | As reported |
| 25 | Update of previous systematic review | Whether described as an update |
| 26 | Databases searched | Count of databases searched |
| 27 | Date of last search | Date; original expects day/month/year |
| 28 | GRADE/CINeMA or similar used | Whether certainty of evidence was assessed |
| 29 | Certainty rating for primary outcome/intervention | Conditional on item 28 |
| 30 | Imprecision of confidence intervals | Assessor judgement based on reported discussion and/or primary-outcome CIs |

Additional columns include review ID, reviewer name/initials, publication year, DOI/PMID, full-text link, objective, primary intervention/exposure, primary outcome, and abstract finding. 

## 5. Evidence, rationales and clarity ratings
Item judgements have linked **verbatim quotation(s)**, **written rationale(s)**, and evidence-clarity coding. 

| Evidence-clarity label | Description used for documentation | Verification needed |
|---|---|---|
| **Clear** | Source evidence clearly supports an interpretable judgement | Confirm exact coding instructions |
| **Weak** | Evidence is vague, incomplete, or difficult to interpret | Confirm distinction from missing evidence |
| **Difference** | Contradictory statements or evidence within the same document | Confirm operational decision rules |
| **No Information** | Relevant information not available in the review and checked associated sources | 

## 6. Source 
For the complete benchmark description, see the repository [README](README.md). For the historical smaller subset, see [WISEST-QA-Dataset](https://github.com/carolelunny/WISEST-QA-Dataset).
