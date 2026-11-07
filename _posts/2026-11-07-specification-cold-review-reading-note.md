---
layout: post
title: "Give the specification a cold review"
summary: "Separate planning, independent review and implementation checks."
date: 2026-11-07
tags: ["Software", "Planning", "ReadingNotes"]
---

**Original reading note, not a complete discussion archive.** Checked 2026-11-07 UTC.

Source: [For over a year I've spent a full day writing a Markdown spec before prompting Claude. Google just open-sourced the "Elephant-Goldfish Model" that takes this 10x further](https://www.reddit.com/r/ClaudeAI/comments/1xkn61s/for_over_a_year_ive_spent_a_full_day_writing_a/), by Reddit user **u/derekleeth**. Coverage: the opening post and a portion of visible replies. Linked announcements, software and collapsed comments were not checked. No permissive reuse license was established; this note paraphrases rather than reproduces the discussion.

## Keep the separation of responsibilities

The author advocates developing a written specification before implementation. The described approach separates a planning conversation, a reviewer that receives the specification without the preceding conversation, and a later comparison of implementation against the specification.

Visible replies challenge the novelty and compare it with established planning practices. That disagreement is useful: the technique should earn its time by revealing concrete omissions. The linked product's capabilities and the title's quantitative claim were not independently verified.

## A small experiment

Write one page containing the problem, constraints, failure cases and acceptance examples. Give only that page to a reviewer. Ask what cannot be implemented unambiguously, rather than whether it sounds good.

Resolve the most consequential uncertainty, implement a small slice, then compare the result with the examples. Record any intentional deviation. Use the experiment's findings to decide whether a larger specification is worthwhile; a full day of planning is not a universal prerequisite.
