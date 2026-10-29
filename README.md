<div align="center">

# System-writing-skills

### A Battle-Tested Writing System for Top-Tier Computer Systems Papers

*Distilled from the writing practice of faculty at Peking University,
Shanghai Jiao Tong University, Nanjing University,
and Huazhong University of Science and Technology*

<br>

[![Domain](https://img.shields.io/badge/domain-Computer%20Systems-2F6FED)](https://github.com/hustxiangyu/System-writing-skills)
[![Format](https://img.shields.io/badge/format-Skill%20Manual-1A7F5A)](https://github.com/hustxiangyu/System-writing-skills/blob/main/SKILL.md)
[![Sections](https://img.shields.io/badge/sections-8-C2691F)](https://github.com/hustxiangyu/System-writing-skills/blob/main/SKILL.md)
[![Principle](https://img.shields.io/badge/principle-Explain%2C%20Don't%20Describe-8B5CF6)](https://github.com/hustxiangyu/System-writing-skills/blob/main/SKILL.md)

[![Language](https://img.shields.io/badge/language-English-333333)](https://github.com/hustxiangyu/System-writing-skills)
[![License](https://img.shields.io/badge/license-CC--BY--4.0-999999)](https://github.com/hustxiangyu/System-writing-skills)

[Overview](#overview) ·
[Modules](#module-map) ·
[Mental Models](#core-mental-models) ·
[Quick Start](#quick-start)

</div>

---

## Overview

Top systems papers do not win on novelty alone — they win on **clarity under time pressure**.
A reviewer must grasp four things in minutes:

| | Question | Where It Lives |
|---|---|---|
| **1** | What did you do? | Title · Abstract · Introduction |
| **2** | Why does it matter? | Introduction · Motivation |
| **3** | Why is it hard? | Introduction · Challenges |
| **4** | Why does it work? | Design · Evaluation |

`System-writing-skills` is a compact, actionable manual that encodes how elite systems papers answer those four questions — section by section, sentence by sentence.

> **The core idea:** *Writing is a long-distance duel with the reviewer.
> Anticipate the objection, close the gap before it is raised.*

---

## Module Map

The manual is organized into four layers — from strategy to pixels.

<table>
<tr>
<td width="50%" valign="top">

### Module 1 · Section Playbook
Every section has a job. This module defines it.

- **Title** — one-sentence identity + memorable system name
- **Abstract** — What / Why / How / So What in 200–250 words
- **Introduction** — the narrative that decides acceptance
- **Background & Motivation** — terminology first, root cause next
- **Design & Implementation** — principles before details
- **Evaluation** — questions first, then ablation & overhead
- **Related Work** — contrast, not a second background
- **Limitation & Conclusion** — confident, honest closure

</td>
<td width="50%" valign="top">

### Module 2 · Sentence Craft
How to write prose reviewers trust.

- One paragraph, one claim — claim first
- Keep sentences under ~25 words
- One term, one meaning — all paper long
- Logical connectives or restructure
- Kill orphaned last lines

### Module 3 · Visual Standards
Figures that carry the paper.

- Figure-first: captions alone should tell the story
- Unified palette · tight caption spacing
- Rigorous, consistent math notation

### Module 4 · AI Discipline
Use AI as a lens, never a voice.

- Never let AI write your first draft
- Polish / grammar / idiom-check only
- Cache-flush re-read before submission

</td>
</tr>
</table>

---

## Core Mental Models

| # | Model | In Practice |
|---|---|---|
| 1 | **Clarity under time pressure** | Lead with what / why / hard / effective |
| 2 | **Anticipate & plug holes** | Pre-answer bias, overhead, generalizability |
| 3 | **Reviewer persona** | A bright broad-area peer — a sharp second-year PhD |
| 4 | **Manage working memory** | Stable terms · modular paragraphs · deliberate repetition |
| 5 | **Explain, don't describe** | Motivation & trade-offs beat procedural narration |

---

## Quick Start

**1 — Read once, end to end.**
[`SKILL.md`](./SKILL.md) is modular and short. One pass builds the map.

**2 — Draft with the matching module open.**
Writing the Introduction? Keep §3 beside you.

**3 — Run the self-check.**
Before submission, use the *cache-flush re-read* from Module 4:
read as an unprepared external reader, sentence by sentence.

```text
For every sentence ask:
  → What is my real intent in writing this?
  → What remains in the reader's working memory?
  → Will this cause ambiguity or misunderstanding?
If information is missing, add the leading text. Now.
```

---

## Repository Structure

```text
System-writing-skills/
├── README.md    ← you are here
└── SKILL.md     ← the complete skills manual
```

---

## Why This Works

| Conventional Advice | This Manual |
|---|---|
| "Write clearly" | Claims-first paragraphs, 25-word discipline, terminology locks |
| "Tell a story" | Conflict → challenge → design → proof, mapped section-to-section |
| "Make good figures" | Captions-alone test, unified palette, tight page rhythm |
| "Use AI to help" | Draft-by-hand rule, AI limited to polish & idiom |

The manual encodes **executable rules**, not aesthetics — so you can audit a draft
against it and find what is wrong in minutes, not days.

---

## Origin

This is an original distillation of multi-university paper-writing practice from the
Chinese computer systems community, reorganized into an actionable skill format.
When guidance conflicts across sources, the Markdown rules in [`SKILL.md`](./SKILL.md) are authoritative.

---

<div align="center">

**Write so the reviewer sees the contribution — before they see the words.**

<br>

[![Read the Manual](https://img.shields.io/badge/Read-SKILL.md-2F6FED?style=for-the-badge)](./SKILL.md)

</div>
