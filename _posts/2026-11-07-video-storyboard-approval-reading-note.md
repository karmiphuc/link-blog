---
layout: post
title: "Storyboard first, render after approval"
summary: "An offline note on an n8n video workflow and its cost-control boundary."
date: 2026-11-07
tags: ["Automation", "Video", "ReadingNotes"]
---

**Original reading note, not a complete source archive.** Checked 2026-11-07 UTC.

Source: [I built this AI automation that generates viral Bigfoot / Yeti vlogs using Veo 3](https://www.reddit.com/r/n8n/comments/1lkbx2b/i_built_this_ai_automation_that_generates_viral/), by Reddit user **u/dudeson55**. Coverage: the written opening post, including its workflow and cost discussion. Linked workflow code, video, images and the complete comment tree were not inspected. No permissive reuse license was established; this is original paraphrase without reproduced prompts or media.

## The useful pattern

A short idea enters an n8n form. A planning stage divides it into eight eight-second scenes; a second stage supplies consistent character, camera, lighting and sound details. Human approval precedes paid rendering. The workflow then submits clips through FAL, polls for completion and places outputs in Google Drive for editing.

The durable lesson is to separate cheap planning from expensive execution. Review the entire storyboard before purchasing clips. The post's historical prices and service behavior are not verified current specifications.

## A reusable review card

Before approving any generated-video job, write down:

1. What happens in each shot, and what changes between shots?
2. Which character and visual details must remain constant?
3. What is the maximum accepted spend, including failed generations?
4. Where will completed clips and their job identifiers be retained?
5. How will an uncertain submission be reconciled before another purchase?

This checklist is an independent application, not executable workflow code. The note works offline; rendering still requires the relevant services and access.
