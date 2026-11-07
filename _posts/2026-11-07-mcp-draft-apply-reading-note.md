---
layout: post
title: "An agent should edit a draft before it applies changes"
summary: "A phone-layout demonstration illustrates a useful tool-permission boundary."
date: 2026-11-07
tags: ["Software", "MCP", "ReadingNotes"]
---

**Original reading note, not a full source or software archive.** Checked 2026-11-07 UTC.

Source: [I gave Claude access to my iPhone Home Screen through MCP and asked it to organize my apps by color](https://www.reddit.com/r/mcp/comments/1xjs7bk/i_gave_claude_access_to_my_iphone_home_screen/), by Reddit user **u/BTCLSD**. Coverage: the opening written post; some visible replies were read, but are not reproduced here. App binaries, screenshots, linked repositories and the complete discussion were not inspected. No permissive reuse license was established; this is original commentary and paraphrase.

## The useful boundary

The author describes Thumbwise reading a phone layout into a Mac app, exposing tools through a local MCP helper, and allowing an assistant to propose a color-based arrangement. The described design uses the same core rules for UI and agent actions. Applying a draft requires permission and a backup; an uncertain response should not trigger a blind repeated write.

These are the author's design claims, not independently tested guarantees. Compatibility, pricing and privacy behavior have not been verified here.

## Apply the pattern elsewhere

For a tool that changes important state:

1. Read the original state and preserve a recovery copy.
2. Let the agent construct a draft with bounded operations.
3. Show a difference that a person can understand.
4. Require the intended permission at the apply boundary.
5. Read the resulting state back. Reconcile a missing response before retrying.

A useful preview is more than a screenshot: it explains exactly which objects will change. This general checklist is independent guidance, not instructions for connecting a phone or installing the demonstrated app.
