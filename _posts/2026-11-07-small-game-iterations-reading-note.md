---
layout: post
title: "Build an AI-assisted game one playable slice at a time"
summary: "A practical reading note on design context, small steps, tests and recoverable checkpoints."
date: 2026-11-07
tags: ["GameDevelopment", "ReadingNotes"]
---

**Reading note, not a full guide copy.** Checked 2026-11-07 UTC.

Source: [Ultimate Guide to Vibe Coding V1.2.2](https://github.com/EnzeD/vibe-coding), Nicolas Zullo. The README records creation on 2025-03-12 and update on 2026-05-25. Coverage: the complete English README, including setup, iteration, debugging and FAQ. Referenced apps, games and services were not tested. No license file was present in the inspected repository tree; this post uses original paraphrase and no substantial verbatim excerpt.

## The durable workflow

Zullo's guide starts with a short game-design document, a deliberate technology choice and an implementation plan broken into testable steps. It keeps design intent, progress and architecture notes alongside the project so that a new coding session can recover context.

The core loop is small: clarify the next step, implement it, check the result and record a checkpoint before moving on. Build the base game before adding decorative features. When an attempt fails, provide concrete error evidence instead of piling more vague requests onto the same conversation.

The source includes specific model, pricing and permission-mode advice. Those are not preserved as current recommendations here, and this note does not recommend bypassing permission checks or discarding unsaved work.

## A playable-slice exercise

This is an adaptation:

1. Define a single interaction: the player acts, the world responds, and success or failure becomes visible.
2. Write how to test that interaction before adding polish.
3. Implement only enough to make the loop playable. Keep the next feature outside the current change.
4. Run it yourself. Record what actually happened, including the failure case.
5. Save a reviewed version-control checkpoint. If another experiment breaks the game, compare it with that working state and preserve uncommitted work before reverting anything.

Keep architecture notes proportional to the project. A short explanation of where state lives and how the loop runs is more useful than elaborate documents that no longer match the code.
