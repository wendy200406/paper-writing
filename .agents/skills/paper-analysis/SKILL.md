---
name: paper-analysis
description: "Analyze philosophical sources and philosophically relevant interdisciplinary sources as arguments, conceptual interventions, interpretations, dialectical moves, cases, or topic maps. Use for philosophy papers, primary texts, monographs, chapters, commentaries, handbooks, and formal or empirical sources when their philosophical role matters; reconstruct concepts, distinctions, arguments, objections and replies, interpretive claims, normative reasoning, and support. Do not use for generic scientific-paper appraisal, systematic-review synthesis, prose drafting, citation-only checks, publication-readiness review, or project-file updates without explicit authorization."
---

# Paper Analysis

Analyze a source according to its genre, method, and argumentative function. Do not reduce every philosophical source to neutral summary or force every source into premise-conclusion form.

## Philosophy-First Boundary

Treat concepts, distinctions, arguments, interpretations, objections and replies, cases and thought experiments, phenomenological descriptions, formal results, normative claims, and dialectical positions as the primary research objects. Philosophical rigor concerns textual fidelity, conceptual precision, inferential or interpretive support, scope and force, objection handling, and responsible placement in a debate.

Do not default to scientific-paper conventions such as hypothesis testing, methods/results appraisal, statistical significance, replicability, data extraction, meta-analysis, or systematic-review synthesis. When empirical or scientific material bears on a philosophical question, identify the result and its warranted scope, then assess the bridge to the philosophical premise or conclusion. Do not let an empirical result by itself settle a conceptual, normative, metaphysical, or interpretive claim; request domain-specific scientific checking when the philosophical assessment depends on technical validity.

## Evidential Layers

Keep these layers explicit:

- the author's explicit claims and stated arguments;
- the author's reports or interpretations of other sources;
- a source-supported reconstruction of what follows from the text;
- an analyst-supplied charitable repair, inference, objection, or evaluation, labeled as such;
- the user's or project's possible use of the source.

Never turn a charitable reconstruction into an attribution. Mark uncertainty as access-limited, textually underdetermined, interpretively disputed, or evaluative rather than hiding it behind a confidence score.

## Routing

- For PDFs, use `pdf` first for access, pagination, extraction, and visual verification.
- For Zotero library lookup, citation records, and bibliography export, use `zotero`.
- For prose drafting from an already analyzed source, use `philosophy-writing`.
- For project-specific use, pair this with a private project extension.
- For project-file updates, stop at use candidates unless the user explicitly authorizes exact targets.

## Task Triage and Modes

Before reading, identify the source object, the user's question, requested depth, source function or genre, available material, project context, citation style, and file-update permission.

Use the narrowest mode that fits:

- `analysis-only`: analyze without project-use proposals or file updates;
- `analysis-plus-handoff-candidates`: analyze and propose later uses without updating project files;
- `analysis-plus-authorized-updates`: update only the exact files or file classes authorized for the current task;
- `topic-map`: map a genuine overview, introduction, textbook, or survey source;
- `hybrid`: map an overview function and closely reconstruct an authored argument in the same source.

If no project context exists, default to `analysis-only`. If project context is supplied, default to `analysis-plus-handoff-candidates` unless the user explicitly authorizes another mode.

## Workflow

1. Identify the source: author, title, year, venue, version, DOI or stable identifier when available, and source path or supplied material.
2. Establish access status: full text, partial text, abstract or excerpt, user notes only, scan/OCR, missing pages, corrupted source, or unreliable extraction.
3. Survey the whole available source before giving a full-source analysis. Do not infer the argument from the title, abstract, introduction, or conclusion alone.
4. Verify printed and PDF pagination before page-specific claims, and inspect notes, figures, tables, appendices, or formal apparatus when they bear on the analysis.
5. Identify the source's question or purpose, thesis or governing claim, dialectical target, structure, method, and debate framing.
6. Choose reading depth from the user's request, source access, source complexity, risk of misinterpretation, and intended use. Do not let a project-relevance score override a requested thorough analysis.
7. Reconstruct central arguments or interpretive moves. Record provenance, conclusion or claim, grounds, inferential or interpretive link, scope and force, hidden assumptions, objections, replies, and unresolved alternatives.
8. Assess separately the inferential link, the conceptual or textual support for each premise or interpretation, the warrant appropriate to each support type, and external criticism.
9. Reconstruct the author's debate-framing profile without converting the author's self-positioning into independently verified field history.
10. Screen the bibliography for verified useful sources and clearly labeled follow-up leads. Never use an unread lead as evidence.
11. Report downstream uses only at the level authorized by the selected mode.

## Genre and Method

Route by function, not publication container:

- argument-driven work: reconstruct claims, grounds, inferences, objections, and replies;
- historical, exegetical, or intellectual-historical work: distinguish primary-text claims, textual evidence, historical-context claims, reception or transmission claims, rival readings, and present philosophical evaluation; record interpretive method, edition or translation issues, conceptual change, and risks of anachronism;
- phenomenological or descriptive work: identify the phenomenon, standpoint, descriptive procedure, and relevant experiential structures; distinguish phenomenological description from introspective report, case narrative, conceptual analysis, causal explanation, and any normative or metaphysical inference; state the claimed scope or generality;
- formal work: state the target informal claim, syntax and semantics, definitions, axioms or assumptions, derivation or proof, model or countermodel, and scope; assess validity, consistency, formalization adequacy, and whether the philosophical interpretation exceeds the formal result;
- normative work: identify the normative question, target, and claim type; reconstruct the reasons, values, principles, duties, permissions, or virtues offered; make bridge principles explicit; distinguish grounding, justifying, weighing, enabling, and defeating roles when relevant; test scope, priority, feasibility, counterexamples, conflicts, and the move from descriptive or conceptual premises to normative conclusions;
- case- or thought-experiment-driven work: record stipulations, imported background assumptions, the target concept or principle, the intended verdict, modal status, and inferential role; test variants, robustness, representativeness, confounds, and whether the case supports the claimed conclusion;
- philosophically relevant empirical work: identify the empirical claim, design, result, and warranted scope only to the depth needed; state the exact philosophical premise, concept, case, objection, or conclusion it bears on; assess the bridge and do not infer normative or metaphysical conclusions from data alone;
- overview, textbook, introduction, or survey work: map topic architecture, distinctions, rival positions, omissions, and the source's organizing narrative.

An authored handbook chapter may be an original argument. Use normal or hybrid analysis unless the chapter actually functions as an overview.

## Optional Project-Relevance Scale

Use this only when the user supplies a project or research question. The score measures prospective use, not philosophical quality or reading depth.

- `5`: central source that materially shapes a thesis, premise, or major objection and reply;
- `4`: direct and substantial use in a live argument, section, or literature review;
- `3`: clear use for a concept, premise, objection, case, or debate narrative;
- `2.5`: borderline; no clear argumentative role yet;
- `2`: limited background or bibliographic use;
- `1`: remote topical overlap;
- `0`: no identifiable use.

Require a concrete prospective role for any score above `2.5`. Omit the score when no project context exists unless the user requests it.

## Source Discipline

- Never invent citations, quotations, page numbers, DOI values, evidence, argumentative steps, or source positions.
- Do not claim full-source analysis unless the full available text was inspected.
- Use page or stable locators for source-specific analytical claims when reliable locators exist.
- Treat OCR and extracted text as provisional for names, symbols, punctuation, footnotes, and quotations until visually checked.
- State what material is missing and what cannot responsibly be claimed from partial access.
- Preserve the source's terminology before introducing an analyst's or project's vocabulary.
- Distinguish internal or immanent criticism from external assessment.
- Use the user's citation style; if none is specified and a formatted reference is needed, default to APA 7.

## References

Read only what the task needs:

- `references/analysis-checks.md`: detailed genre, attribution, concept, argument, interpretation, evidence, and literature-placement checks;
- `references/report-templates.md`: thorough, concise, provisional, and adaptable report structures;
- `references/bibliography-and-handoff.md`: bibliography screening and use-candidate formats.

## Output

For chat-only answers, lead with source access, reading depth, source function, core thesis or purpose, main argumentative or interpretive contribution, strongest unresolved problem, and next step. Include project relevance only when project context exists.

For saved reports, include enough provenance, locators, and layer labels for later verification. State whether objections and repairs are author-raised, source-supported reconstructions, or analyst-generated.
