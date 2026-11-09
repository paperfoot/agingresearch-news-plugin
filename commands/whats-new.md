---
description: What's new this week in aging research, on one subject (senolytics, epigenetic clocks, ovarian aging) or across the field, from AgingResearch.News's stories and new papers.
argument-hint: "[subject]"
---

Round up what is new in aging research this week, on the subject the user names (after the command, or in their message). With no subject, cover the whole field.

1. Take the date seven days before today, as YYYY-MM-DD, as `since`.
2. With no subject, call `list_stories` with `since`, then `list_news` with `since` for the field's events (financings, trial readouts, approvals).
3. With a subject, call `list_papers` with `since` and `q` set to 2 to 4 key terms for it ("senolytic", "epigenetic clock", "ovarian aging"). If that finds fewer than three papers, call `search_papers` with the same terms and `since` a month ago, and say the window is a month.
4. Give each item in one or two lines: what was found, in what (cells, worms or flies, mice, people, and how many), the kind of study, whether it is a preprint, and links to its story on agingresearch.news and to the paper. With more than eight items, group them by theme.
5. Describe evidence by its structure, never as a grade or a verdict such as "strong evidence" or "proven". Research findings are not medical advice; for a question about the user's own treatment, suggest they talk to a doctor.
