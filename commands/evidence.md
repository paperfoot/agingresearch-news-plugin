---
description: The evidence on a drug, supplement, diet, gene or process in aging (rapamycin, metformin, NAD+ precursors, taurine), laid out by the species it has reached, independent replication, findings against, trials and funders, from AgingResearch.News.
argument-hint: "<drug, supplement, gene or process>"
---

Lay out the evidence on the drug, supplement, diet, gene or process the user names (after the command, or in their message). If they name none, ask which one they mean.

1. Call `find_entities` with `q` set to the name. Take the entity the name matches exactly; if several fit equally (a drug and a gene of the same name), ask which one.
2. Call `get_entity` with its `type` and `key`. Its `evidence` holds the structure: the species reached, whether independent labs found the same there, the labs and countries, findings against, trials and how many posted results, funders and company ties.
3. Call `list_claims` with the key as `subject` for what papers found and in which organisms, such as lifespan in mice.
4. Call `list_trials` with `q` set to the name for trials in people, and note which are recruiting.
5. Answer in this order: one sentence on how far the evidence has reached (for example, lifespan extended in mice by several independent labs, with no trial in people measuring aging yet); then species and replication; findings against; trials; funders and company ties; the three to five newest papers, each with its link on agingresearch.news and to the paper, saying which are preprints.
6. Never turn the evidence into a grade or a verdict such as "strong", "weak" or "proven". Research findings are not medical advice; for questions about the user's own dose or treatment, give what the research shows and suggest they talk to a doctor.
