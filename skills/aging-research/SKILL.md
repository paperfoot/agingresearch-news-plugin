---
name: aging-research
description: Use when the user asks about aging or longevity research - what the evidence says on a drug, supplement, diet, gene or process (rapamycin, metformin, senolytics, NAD+, GLP-1 drugs, caloric restriction), biomarkers of aging such as epigenetic clocks, clinical trials in aging and age-related disease, new papers and preprints in the field, research grants, longevity industry news or drug programs in development - or asks to follow a topic on AgingResearch.News. Answers with the AgingResearch.News connector's tools, which read new papers on aging every day and judge each one for its link to aging.
---

# Aging research with AgingResearch.News

AgingResearch.News reads new papers on aging and age-related disease every day, judges each one for its link to aging and writes short stories about the ones worth reading. Its tools read its own database.

## Which tool for which question

| The user asks | Call |
|---|---|
| What the evidence says about a drug, supplement, diet, gene or process ("does rapamycin slow aging?") | `find_entities` to get the type and key if unsure, then `get_entity`. Its `evidence` is the structure of the evidence: the species reached (cells, worms or flies, mice, humans) and whether independent labs replicated it there, labs and countries, findings against, trials and those with no results posted, funders, company ties |
| What is new across the field (today, this week) | `list_stories` with `since` (its checked stories), `list_news` for the field's events |
| What is new on one subject | `list_papers` with `q` (2 to 4 key terms) and `since`, or `search_papers` for a longer window; `list_stories` has no subject filter |
| About one paper | `search_papers` to find it, then `get_paper` with its AgingResearch.News id |
| Specific findings, such as what extends lifespan in mice | `list_claims` |
| Clinical trials | `list_trials` (filter by words, phase, status), then `get_trial` |
| Industry news, funding rounds, approvals | `list_news` |
| Research funding | `list_grants` |
| Meetings and abstracts | `list_conferences`, `get_conference` |
| Drug and therapy programs in development | `list_assets`, `get_asset`, `count_pipeline` |
| To follow or stop following a topic | `follow` / `unfollow` with the type and key from `find_entities`; `list_follows` to show them |
| A research question that needs a written answer with sources | `ask_arn` (needs the user's account); `get_ask_answer` to collect an answer that is still being written |
| A full review of the evidence on a research question, beyond a short answer | `start_ultradeep` (needs the user's account; it takes several minutes), then `get_ask_answer` |
| Their earlier questions to AgingResearch.News | `list_questions` |

## How to answer

- Describe evidence by its structure, as the tools return it: which species, how many independent labs, what was found against it, which trials posted results. Do not turn it into a grade or a verdict such as "strong evidence" or "proven".
- Say whether a paper is a preprint, and what kind of study it is (in cells, in mice, in people; trial or observational).
- Link each claim to its source: the story on agingresearch.news, the paper, or the registry entry.
- Research findings are not medical advice. For questions about a person's own treatment or dose, give what the research shows and suggest they talk to a doctor.
- Following topics and listing questions need the user's AgingResearch.News account; the tool asks them to sign in when it does. In Claude Code, when a tool says sign-in is needed (or the server shows as needing authentication), tell the user to run `/mcp`, choose agingresearch-news, then Authenticate: a free account gives 100 lookups a day. Drug and therapy programs answer every caller: an outline of each (as AgingResearch.News's asset pages show it) without an account whose plan includes them, the full record with one.
