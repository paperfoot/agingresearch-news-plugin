---
description: Clinical trials in aging and age-related disease for a condition, drug or target (sarcopenia, menopause, senolytics, GLP-1 drugs), showing which are recruiting and each one's phase, sponsor and size, from AgingResearch.News.
argument-hint: "<condition, drug or target>"
---

Find the clinical trials on the condition, drug or target the user names (after the command, or in their message). If they name none, ask which one they mean.

1. Call `list_trials` with `q` set to 1 to 3 key words for it and `status` `recruiting`. If the user names a phase, pass `phase` too.
2. Call `list_trials` again with the same words and `status` `completed` for the trials that have finished.
3. If either finds nothing, try fewer or broader words once, then say so plainly.
4. For the two or three trials that matter most to the question, call `get_trial` for its outcomes, dates and the papers that cite it.
5. Show the trials as a table: registry number (linked), title, phase, status, lead sponsor, size and its latest change. Below it, say in a sentence or two what the papers citing the completed trials report, from `get_trial`, and which completed trials have no paper yet.
6. Research findings are not medical advice; for a question about joining a trial, point the user to the registry entry and its contacts.
