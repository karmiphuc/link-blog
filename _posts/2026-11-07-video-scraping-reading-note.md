---
layout: post
title: "Video scraping: extract data, then check it"
summary: "A small workflow for turning visible information into structured data without losing the verification step."
date: 2026-11-07 08:32:00 +0000
tags: ["AI", "ReadingNotes"]
---

**Reading note, not a complete original archive.** Checked 2026-11-07 UTC.

Source: [Video scraping: extracting JSON data from a 35 second screen capture for less than 1/10th of a cent](https://simonwillison.net/2024/Oct/17/video-scraping/), Simon Willison, 2024-10-17.

Coverage: article body and its December 2024 reliability update read. Embedded images, external tools and the linked conversation were not reproduced or tested. No full-text reuse license was verified; this is original summary text.

## The useful idea

Willison recorded a small screen region while opening twelve emails, pausing on each. Gemini converted the recording into dated monetary records, then CSV. He replayed the video to check every number. The important result is a convenient capture method plus verification, not proof that video extraction is automatically accurate.

The article's tiny cost estimate concerns a particular 2024 model and token price. It is historical, not a current quote. The article also raises data-training and prompt-injection concerns; account-wide access is a different exposure from a deliberately selected recording.

## Workflow to keep offline

1. Decide which fields are needed before recording.
2. Capture only information you are permitted to process. Exclude unrelated personal or access-bearing details.
3. Pause long enough for each record to be legible.
4. Request a fixed schema, including date format and numeric units.
5. Compare the output with the recording before calculating or importing it. Check for omitted and duplicated rows, not just wrong values.

The final two checks are a practical extension of the author's manual comparison. For larger or consequential jobs, an unverified sample is not equivalent to checking every record. Keep uncertain values visibly unresolved.
