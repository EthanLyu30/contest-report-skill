---
name: contest-report
description: Use when drafting, revising, or polishing a Chinese university computer design contest software design and development document, especially "软件应用与开发类作品设计和开发文档", local organizer or teacher docx templates, and reports that must map material into sections such as 需求分析, 概要设计, 详细设计, 测试报告, 安装及使用, 项目总结, and 参考文献.
---

# Contest Report

## Overview

Use this skill when the document must read like a polished Chinese competition submission instead of a generic enterprise PRD or SRS. It adapts SRS, PRD, and architecture material into contest-ready Chinese prose, tables, diagrams, and final docx or pdf deliverables.

## Workflow

1. Read the local contest template and submission requirement files first. Treat chapter names, length hints, and deliverable format as hard constraints.
2. Decide the current objective before writing:
   - full outline
   - one section draft
   - revision of an existing draft
   - final formatting and export
3. When the user provides Word or PDF source documents, inspect not only the text but also the embedded figures, screenshots, table style, caption position, heading hierarchy, paragraph rhythm, and how the original team presents itself. Reuse good source visuals before generating new diagrams.
4. If the user provides both a polished baseline document such as an AIC technical report and a newer milestone, quarterly, or progress report, treat the newer report as the source of truth for recently completed functions, interfaces, deployment constraints, and fresh technical progress.
5. Gather source material into these buckets:
   - project background and practical significance
   - target users and usage scenarios
   - module boundaries and workflow
   - interfaces, data, and database
   - key algorithms or technical innovations
   - tests, metrics, and fixes
   - installation, deployment, and typical usage
   - team division, project reflections, and next steps
6. Map the material into the contest sections using `references/contest-template-map.md`. Keep the contest's Chinese chapter names instead of rewriting the document as a generic English SRS.
7. Raise rigor selectively:
   - borrow requirement precision from `jam01/SRS-Template`
   - borrow design structure from IEEE 1016 and software design document templates
   - borrow discovery and architecture thinking from business analyst, product manager, and architect style workflows
   - borrow security and privacy questions for sensitive or medical systems
8. Write concise Chinese academic prose. Prefer figures, tables, UML, ER, flowcharts, and real screenshots over long explanation blocks, especially in 概要设计 and 详细设计.
9. When the template asks for a short section, compress by increasing information density rather than by deleting all specificity. Prefer combined figure boards, compact comparison tables, and short synthesis paragraphs over hollow prose.
10. When generating Chinese `.docx` content programmatically, avoid shell-embedded non-ASCII code blocks that can be downgraded to `?` by the console code page. Prefer UTF-8 script files, relative workspace paths, and a post-save reopen check on the generated document.
11. If the user needs a final `.docx` or PDF, use the `doc` skill for document editing and the `pdf` skill for render checks before delivery.

## Trigger Cases

Use this skill when the user asks for things like:

- 写计设赛设计和开发文档
- 按比赛模板写需求分析/概要设计/详细设计
- 把现有 markdown 或笔记改成比赛文档
- 润色“软件应用与开发类作品设计和开发文档”
- 把项目材料整理成正式参赛文档
- 针对老师或组委会给的 docx 模板补全内容

## Writing Rules

- Keep the contest chapter names exactly as provided by the template unless the user explicitly asks to rename an internal heading.
- Treat chapter title hierarchy explicitly. The main contest chapter titles such as `第一章 需求分析` and `第二章 概要设计` may remain centered, but internal subheadings should normally be left aligned. Use at most three levels, and prefer two levels when the material is not dense enough to justify deeper nesting.
- If the user or local template expects numbered main chapters, use full chapter titles such as `第一章 需求分析` rather than bare section names.
- Write as the project team submitting the work, not as an outside assistant summarizing source files. Prefer `我们设计…` / `我们将平台定位为…` and avoid meta phrases such as `结合技术报告可以看出…`.
- Prefer formal Chinese academic style over startup pitch language.
- Translate technical novelty into score-relevant language: feasibility, completeness, innovation, workload, demonstrability, and practical value.
- Keep every requirement, metric, and test statement observable. Replace vague wording such as "good", "friendly", or "high efficiency" with concrete conditions, thresholds, flows, or comparison points.
- Do not let the document become a full enterprise SRS. Borrow rigor from SRS and architecture templates, but compress it into contest form.
- Explain why major technologies were chosen, not just what they are.
- Make diagrams earn their place. Every figure or table should clarify structure, flow, comparison, data design, or test evidence.
- Prefer visuals extracted from the user's own source documents when they are already good enough. Only generate a new figure when the source materials do not provide a usable one.
- If a new figure must be generated, keep all labels fully inside shapes, keep arrows tidy, and avoid cluttered crossings.
- Do not write process explanations as stiff AI-style `1. 2. 3.` bullets unless the user explicitly asks for a numbered list. Prefer connected prose that introduces a figure or a table naturally.
- Avoid formulaic connective chains such as repeated `首先` / `然后` / `最后` or rigid `一是` / `二是` / `三是` summaries unless the material truly requires explicit enumeration. Good contest prose should read naturally and vary its sentence rhythm.
- Avoid dialogue-like wrap-up lines that sound as if the writer is speaking to the reader about the writing process, such as `这一章把……交代清楚了` or `接下来我们……`. Section endings should still read as part of the submitted document.
- Put figure and table titles below the object, and make sure the body text explicitly references them with phrases such as `如图x-x所示` or `如表x-x所示`.
- Treat explicit user or template typography requirements as hard constraints, including fonts, paragraph indentation, alignment, and spacing.
- Unless the user explicitly wants spacing for readability, do not leave extra spaces between Chinese and adjacent English, numbers, or symbols in the final Chinese prose.
- Do not let 概要设计 become too thin. It should surface the real high-level technical focus, not just repeat one architecture paragraph and one module table.
- Do not let a section become "title-only". `需求分析` should usually close with a short summary paragraph that gathers the chapter's argument, and `概要设计` should usually show more than one kind of evidence when the source documents allow it.
- If a chapter summary is only one short paragraph and the template is page-constrained, fold it into the chapter ending instead of creating a separate `本章小结` subheading.
- When the source documents contain real platform screenshots, especially WSI annotation interfaces, task pages, or result views, prefer those screenshots in `概要设计` instead of relying only on architecture diagrams. Architecture alone is usually insufficient.
- If several screenshots are all relevant but the template page budget is tight, prefer a clean combined figure board over deleting recent progress entirely.
- When multiple extracted media folders exist, bind source images explicitly by document and purpose instead of relying on ambiguous directory auto-selection.
- After rendering the final docx or PDF, look for awkward short wrap lines. If a rewritten paragraph leaves only one or two Chinese characters, or an obviously broken caption fragment, hanging on the next line, revise the wording or figure caption instead of leaving the line break as-is.
- Do not overuse a single subject term such as `平台`. When the meaning stays the same, vary references naturally across `医标智绘`、`本作品`、`系统`、`该协作平台` and similar expressions, but keep the referent clear.
- If the project has two members or clear module ownership, make the module boundaries and interface boundaries visible enough to support later evaluation.

## Section Strategy

For section-specific guidance, always read `references/contest-template-map.md`.

Default stance by section:

- `需求分析`: explain why this project should exist, who uses it, what problem it solves, what the main functions are, and how it compares with alternatives.
- `概要设计`: show system modules, their relationships, external interfaces, and the overall human-computer interaction path.
- `详细设计`: focus on real UI pages, database design, core workflows, key algorithms, and technical highlights.
- `测试报告`: show representative test cases, bug-fix loops, and measurable indicators rather than generic testing theory.
- `安装及使用`: keep the deployment environment, setup path, and typical workflow short and executable.
- `项目总结`: reflect on engineering difficulty, teamwork, lessons learned, and future evolution, not generic feelings.

## Medical And AI Projects

If the system involves medical images, model-assisted annotation, AI inference, or sensitive data, read `references/medical-ai-project-guide.md`.

At minimum, make the document explicit about:

- who uploads, annotates, reviews, and exports data
- what data is stored and how it is de-identified or protected
- where AI assists the workflow and where humans remain in control
- what happens when the model is uncertain or wrong
- which quantitative indicators matter for usability, accuracy, and efficiency

If the user asks for deeper security or privacy treatment, combine this skill with `security-threat-model`.

## Quality Bar

Before final delivery, read `references/quality-checklist.md`.

The report is not ready until:

- every chapter clearly answers the contest template's prompt
- the design sections contain enough structure, not just prose
- the test section contains evidence and metrics, not slogans
- the language sounds like a judged submission, not brainstorming notes
- the final file renders cleanly in docx or PDF form if delivery files are requested
- any newly generated Chinese content survives a save-and-reopen check without mojibake or mass `?` replacement

## Source Stack

Use `references/source-stack.md` when deciding which external method or template to borrow from.

Short rule of thumb:

- use contest templates as the hard outer shell
- use SRS templates to strengthen requirement precision
- use design document templates to strengthen architecture and data sections
- use PM and architect workflows to improve logic, not to impose enterprise ceremony

## Maintenance Rule

This skill is expected to evolve with real contest work.

When later turns reveal repeated judge concerns, better section patterns, stronger tables, or clearer medical AI language:

- update the relevant reference file first
- update `SKILL.md` only when the core workflow should change
- prefer small, cumulative improvements over rewriting the skill from scratch
