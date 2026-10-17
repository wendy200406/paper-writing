# Paper Analysis Skill

`paper-analysis` is a project-neutral Codex skill for source-grounded philosophical research. It analyzes philosophical texts and philosophically relevant interdisciplinary material by reconstructing concepts, distinctions, arguments, objections and replies, interpretations, cases, normative reasoning, and dialectical roles. Empirical findings are one possible kind of support for a philosophical premise or conclusion, not the default model of inquiry.

## Quick Workflow

1. State what source material is actually available.
2. Identify the source's function or genre and the user's question.
3. Survey the whole available source before claiming a full reading.
4. Choose depth from the request, access, complexity, and interpretive risk.
5. Reconstruct the source without merging attribution, charitable repair, and evaluation.
6. Check concepts, support, scope, objections, and debate framing.
7. Screen bibliography leads and propose project uses only at the authorized level.

Project relevance is optional and separate from reading depth. A low-relevance source can still receive a thorough analysis when the user requests one or the source is foundational, complex, or interpretively risky.

## Public Skill vs. Private Extension

This repository contains only the reusable method. Keep private research claims, personal paths, project status, local templates, and file-update policies in a separate project extension.

A private extension can look like:

```text
project-paper-analysis/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── project-context.md
    ├── report-template.md
    └── write-policy.md
```

The extension may set a default report destination or authorize bounded updates. It should not weaken the general skill's source discipline or copy private content back into this public repository.

## Deploying a Personal Project Skill

Use a personal project skill when you want `paper-analysis` to support a specific research project without putting private material in this public repository. The personal skill should act as a thin adapter: it supplies project context, report conventions, and write permissions, while this public skill supplies the general reading method.

Recommended private structure:

```text
my-project-paper-analysis/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── project-context.md
    ├── analyze.md
    ├── classify.md
    ├── integrate.md
    ├── report-templates.md
    ├── write-policy.md
    └── large-multi-source-passes.md
```

Deploy it locally:

```bash
mkdir -p ~/.codex/skills/my-project-paper-analysis/agents
mkdir -p ~/.codex/skills/my-project-paper-analysis/references
```

Then create the files above. Keep `SKILL.md` short and make it route by mode:

```markdown
---
name: my-project-paper-analysis
description: "Use only when a source is being analyzed, classified, or integrated for [project name]. Pair with paper-analysis for the general reading method. Do not use for unrelated paper analysis or unauthorized file updates."
---

# My Project Paper Analysis

Use `paper-analysis` for source access, philosophical reconstruction, debate framing, evidence checks, and bibliography screening. This personal skill supplies only project context, report conventions, and permissions.

Before retrieval, select exactly one mode:

- `analyze`: read `references/analyze.md`, `references/project-context.md`, and `references/write-policy.md`; read `references/report-templates.md` only when creating or updating a durable report.
- `classify`: read `references/classify.md` when deciding a disputed or high-stakes source role.
- `integrate`: read `references/integrate.md` and `references/write-policy.md`; use only when the user explicitly authorizes the exact target file or file class.

Record this packet before reading or writing project material:

```text
Mode:
Source or report:
Project context:
Read set:
Write set:
Authorized output:
File-update permission:
Stop condition:
Proposed durable result:
```

If a task spans modes, run them in order and reset the read set, write set, authorized output, and stop condition before each mode switch.
```

Create `agents/openai.yaml`:

```yaml
interface:
  display_name: "My Project Paper Analysis"
  short_description: "Analyze and route project sources"
  default_prompt: "Use $my-project-paper-analysis with $paper-analysis to select analyze, classify, or integrate mode under the current permissions."
```

To check deployment, start a new Codex session or reload skills if your environment requires it, then run a small test prompt:

```text
Use $my-project-paper-analysis with $paper-analysis to analyze this abstract only. Do not update files. State the selected mode, read set, write set, and stop condition first.
```

Use the reference files this way:

| File | Purpose |
| --- | --- |
| `project-context.md` | Stable project question, core terms, accepted commitments, tentative hypotheses, and open questions. |
| `analyze.md` | How to apply project relevance criteria after the source has been reconstructed. |
| `classify.md` | How to decide whether a source is a target, ally, objection, background source, method source, or follow-up lead. |
| `integrate.md` | How authorized source material may enter project notes, reports, outlines, or drafts. |
| `report-templates.md` | Private report format, metadata fields, and naming conventions. |
| `write-policy.md` | What may be read, created, updated, or left as a proposal only. |
| `large-multi-source-passes.md` | Optional rules for edited volumes, source clusters, reading lists, or many-source reviews. |

Before using or sharing the personal skill:

1. Verify that the description triggers only for this specific project.
2. Check that general paper-reading rules are not duplicated from `paper-analysis`.
3. Confirm that every long project detail lives in `references/`, not in `SKILL.md`.
4. Confirm that notes, reports, and project claims are context, not independent scholarly evidence.
5. Require verification before promoting claims from unread or second-hand sources.
6. Test with one ordinary source, one disputed source-role case, and one unauthorized update request.
7. Scan the entire folder for personal names, absolute paths, unpublished claims, draft prose, and institution-specific details before publishing anything.

Keep the personal skill private by default. If you later publish a template, replace project facts with placeholders and remove all local paths, identifiers, and private claims.

## Installation

Clone the repository into the Codex skills folder:

```bash
git clone https://github.com/Aaronlves/paper-analysis-skill.git ~/.codex/skills/paper-analysis
```

The operational bundle is:

```text
paper-analysis/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── analysis-checks.md
    ├── bibliography-and-handoff.md
    └── report-templates.md
```

`README.md` is user-facing documentation; Codex follows `SKILL.md` and loads references as needed.

## Use It For

- full-text, excerpt-only, abstract-only, or metadata-limited analysis;
- thesis, purpose, argument, interpretation, concept, objection, and evidence reconstruction;
- debate-framing and rival-view mapping;
- historical or exegetical interpretation;
- phenomenological or descriptive analysis;
- formal or empirical material with philosophical significance;
- genuine overview, textbook, introduction, and survey topic maps;
- bibliography screening and project-use candidates.

Optional companion skills:

- Use `pdf` for PDF access, extraction, pagination, OCR, and visual verification.
- Use `zotero` for Zotero library lookup, citation records, and bibliography export.
- Use `philosophy-writing` when a completed analysis becomes prose drafting or revision.

Do not rely on this skill for generic citation-only checks, publication-readiness review, or project-file updates unless the user separately authorizes those tasks.

## Reading Modes

| Mode | Use |
| --- | --- |
| `analysis-only` | Analyze without project-use proposals or file updates. |
| `analysis-plus-handoff-candidates` | Analyze and propose later uses without writing project files. |
| `analysis-plus-authorized-updates` | Update only exact targets authorized for the current task. |
| `topic-map` | Map a genuine overview, textbook, introduction, or survey source. |
| `hybrid` | Combine topic mapping with close analysis of an authored argument. |

Authored handbook chapters are not automatically surveys. Route by the chapter's function, not its container.

## Evidential Layers

The skill keeps separate:

- what the author explicitly claims;
- what the author reports about other sources;
- what a source-supported reconstruction adds;
- what the analyst supplies as charitable repair, objection, or evaluation;
- what a user or project may responsibly use the source for.

This matters because a stronger charitable argument may be philosophically useful without being textually attributable to the author.

## Example Prompts

```text
Use $paper-analysis to analyze this paper thoroughly. Separate the author's explicit argument, your reconstruction, and your evaluation.
```

```text
Use $paper-analysis on this excerpt only. State what cannot be established without the full text.
```

```text
Use $paper-analysis to assess this authored handbook chapter. Decide from its function whether it needs argument analysis, a topic map, or both.
```

```text
Use $paper-analysis to map this historical interpretation, its textual evidence, rival readings, and philosophical significance.
```

## Validation

After changing the skill, run the current Codex skill validator if one is available.

Also verify that every reference named in `SKILL.md` exists and that `agents/openai.yaml` still matches the trigger and workflow. Basic structural validation does not detect reference drift, duplicated instructions, privacy leakage, or semantic routing conflicts.

## Privacy

Before publishing changes, scan for personal names, absolute local paths, institutional details, unpublished arguments, draft prose, and project-specific terminology. Keep public examples philosophically neutral and clearly generic.
