---
layout: post
title: "AI use cases: choose the supervision boundary"
summary: "A practical reading note on autonomous agents, expert copilots and narrow pipeline components."
date: 2026-11-07 08:32:00 +0000
tags: ["AI", "ReadingNotes"]
---

**Reading note, not a complete original archive.** Checked 2026-11-07 UTC.

Sources: [The 3 AI Use Cases: Gods, Interns, and Cogs](https://www.dbreunig.com/2024/10/18/the-3-ai-use-cases-gods-interns-and-cogs.html), Drew Breunig, 2024-10-18; [Simon Willison's commentary](https://simonwillison.net/2024/Oct/20/gods-interns-and-cogs/), 2024-10-20.

Coverage: both article bodies read; linked demonstrations were not tested. Breunig's page displays CC BY-NC 4.0. This post paraphrases and adds a checklist; it does not reproduce the article or its image. No blanket reuse permission was verified for Willison's commentary.

## What is worth keeping

Breunig separates three kinds of AI work by responsibility. **Gods** aim at general, autonomous human replacement. **Interns** help an expert who can evaluate and correct their work. **Cogs** perform a narrow task inside a larger system, with little ongoing supervision and therefore little room for error. Entertainment tools form a less demanding subgroup.

Willison emphasizes supervised coding help and small components such as transcription or structured extraction. A useful distinction is whether someone actually checks each answer. An impressive demo does not establish dependable unattended operation.

## A checklist to use later

This is an application of the framework, not a quoted procedure:

1. Write down the input, output and person responsible for accepting it.
2. If a competent reviewer must inspect every result, budget that review as part of the task.
3. For an unattended component, define a narrow output contract, a validation check and a failure route before connecting it to consequential actions.
4. Test ordinary inputs and awkward exceptions separately. Keep examples that failed.
5. Describe the actual supervision arrangement when comparing products. Do not let the same word, agent, hide different promises.

The category is a design aid, not a reliability certificate. These are 2024 arguments, not a claim about current model capability.
