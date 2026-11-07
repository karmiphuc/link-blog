---
layout: post
title: "Cognitive load: make the next change easier to understand"
summary: "Reading notes on useful abstractions, honest names and review from an unfamiliar reader."
date: 2026-11-07 08:32:00 +0000
tags: ["Development", "ReadingNotes"]
---

**Reading note, not a complete original archive.** Checked 2026-11-07 UTC.

Primary source: [Cognitive load is what matters](https://github.com/zakirullin/cognitive-load), Artem Zakirullin. The repository identifies the text as a living document and displays CC BY 4.0. This post is an attributed paraphrase and practical adaptation, not a verbatim copy.

Discussion: [Hacker News thread](https://news.ycombinator.com/item?id=45074248), submitted 2025-08-30. Coverage: selected article sections on conditionals, modules, services and familiarity; opening discussion branches about names and early returns. The entire comment tree and external examples were not reviewed. No reuse license was verified for comments; none are quoted.

## What is worth keeping

Zakirullin argues that maintainability depends on how much context a reader must hold while making a change. Necessary domain difficulty differs from confusion introduced by the design. Descriptive intermediate values and simpler control flow can help. Splitting a system into many tiny abstractions can make it harder: a short function still has a cost if understanding it requires following several others. Network boundaries add their own debugging burden.

Familiarity is a trap. Someone who designed the system may no longer notice the mental work imposed on a newcomer.

The discussion adds useful disagreement. defanor questions universal claims about simplicity; dsego argues for names that accurately describe the tested condition. Other participants favor named conditions and early exits. Treat these as competing judgments, not measured consensus.

## A review exercise

This is an adaptation for a real change:

- Ask an unfamiliar teammate to explain the relevant path before explaining it yourself.
- List the files, services and implicit rules they need to visit.
- Remove one unnecessary lookup or misleading name, then repeat the explanation.
- Check cleanup and error behavior before introducing early returns.

Optimize for a reader completing a task correctly, not for a smaller line count. The source uses cognitive load informally; its working-memory illustration is not a precise engineering limit.
