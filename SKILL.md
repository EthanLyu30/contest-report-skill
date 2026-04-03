---
name: contest-report
description: Use when drafting, revising, or polishing a Chinese university competition-style software design and development document, especially documents that follow contest, capstone, innovation, or teacher-issued templates and must map material into sections such as 需求分析, 概要设计, 详细设计, 测试报告, 安装及使用, 项目总结, and 参考文献.
---

# Contest Report

## Overview

Use this skill when the document must read like a polished Chinese competition or project submission instead of a generic enterprise PRD or SRS. It adapts SRS, PRD, and architecture material into contest-ready Chinese prose, tables, diagrams, and final docx or pdf deliverables.

## Workflow

1. Read the local contest template and submission requirement files first. Treat chapter names, length hints, and deliverable format as hard constraints.
   - If the organizer or teacher gives explicit typography rules such as `一级标题二号黑体、二级标题三号黑体、正文五号宋体`, those rules override any default house style from earlier drafts.
   - When the organizer expects pure `宋体/黑体` formatting, do not keep an older mixed-font habit such as `中文宋体、英文数字Times New Roman`; the official contest format wins.
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
   - repository-backed deployment facts and runnable usage steps when the report contains `安装及使用`
6. Map the material into the contest sections using `references/contest-template-map.md`. Keep the contest's Chinese chapter names instead of rewriting the document as a generic English SRS.
7. If the user already has a partially satisfactory chapter, treat that chapter as a baseline to migrate and refit instead of rewriting it from scratch just to unify the voice.
8. Raise rigor selectively:
   - borrow requirement precision from `jam01/SRS-Template`
   - borrow design structure from IEEE 1016 and software design document templates
   - borrow discovery and architecture thinking from business analyst, product manager, and architect style workflows
   - borrow security and privacy questions for sensitive or medical systems
9. Write concise Chinese academic prose. Prefer figures, tables, UML, ER, flowcharts, and real screenshots over long explanation blocks, especially in 概要设计 and 详细设计.
10. When the template asks for a short section, compress by increasing information density rather than by deleting all specificity. Prefer combined figure boards, compact comparison tables, and short synthesis paragraphs over hollow prose.
11. When generating Chinese `.docx` content programmatically, avoid shell-embedded non-ASCII code blocks that can be downgraded to `?` by the console code page. Prefer UTF-8 script files, relative workspace paths, and a post-save reopen check on the generated document.
12. If the user needs a final `.docx` or PDF, use the `doc` skill for document editing and the `pdf` skill for render checks before delivery.

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
- Treat the chapter number prefix as part of the visible title, not as disposable decoration. If the template's automatic heading numbering makes `第一章` differ in font, size, or weight from the chapter name, replace that mechanism and render the whole title in one consistent Songti third-size style.
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
- In page-constrained chapters, do not default to equal-width table columns. Allocate width by information density so that dense explanatory columns get more space and short label columns stay narrow.
- Keep tables as intact as possible. Avoid letting a table split across pages, and try to keep the table body and its below-caption on the same page; only allow跨页 when the content truly cannot fit after compaction.
- When tables still look too tall, compact them in this order: shorten cell wording, reduce internal cell margins and paragraph spacing, then rebalance column widths. Do not leave a bloated table simply because the columns were adjusted once.
- If a page shows a large avoidable blank block before a table or figure, do not assume the content is merely "too long". Check for inherited manual page breaks, keep-with-next chains, or other template residue before rewriting the prose.
- Do not rely on a table style name alone for visible borders. If the rendered effect still looks borderless, set explicit table border XML so the final PDF keeps clear grid lines.
- Treat explicit user or template typography requirements as hard constraints, including fonts, paragraph indentation, alignment, and spacing.
- If the competition requirement gives a document-wide format rule, that rule overrides earlier default formatting preferences for body text, title fonts, or spacing.
- If the official format says `正文五号宋体` or similar, apply that font family consistently to the final visible runs instead of keeping a half-overridden style that still shows `SimSun` or mixed western fonts in Word.
- When Word still appears to show a `SimSun`-style alias after restyling, clear theme-font residue and verify the reopened `Normal` and heading styles carry explicit `宋体/黑体` rFonts rather than assuming the first save was enough.
- When the source draft already contains a later chapter the user considers acceptable, migrate its substance, figures, and structure into the current version instead of rewriting it from scratch.
- When a teacher or organizer raises anonymity concerns, inspect both visible content and file metadata. Cover-page blanks are not enough; also check Word core properties, PDF metadata, review markup state, and any accidental personal identifiers in screenshots or repository paths.
- Unless the user explicitly wants spacing for readability, do not leave extra spaces between Chinese and adjacent English, numbers, or symbols in the final Chinese prose.
- Do not let 概要设计 become too thin. It should surface the real high-level technical focus, not just repeat one architecture paragraph and one module table.
- Do not let a section become "title-only". `需求分析` should usually close with a short summary paragraph that gathers the chapter's argument, and `概要设计` should usually show more than one kind of evidence when the source documents allow it.
- If a chapter summary is only one short paragraph and the template is page-constrained, fold it into the chapter ending instead of creating a separate `本章小结` subheading.
- When the source documents contain real platform screenshots, especially WSI annotation interfaces, task pages, or result views, prefer those screenshots in `概要设计` instead of relying only on architecture diagrams. Architecture alone is usually insufficient.
- If several screenshots are all relevant but the template page budget is tight, prefer a clean combined figure board over deleting recent progress entirely.
- When multiple extracted media folders exist, bind source images explicitly by document and purpose instead of relying on ambiguous directory auto-selection.
- After rendering the final docx or PDF, look for awkward short wrap lines. If a rewritten paragraph leaves only one or two Chinese characters, or an obviously broken caption fragment, hanging on the next line, revise the wording or figure caption instead of leaving the line break as-is.
- If a chapter has a tight page budget, prefer merging a short concluding thought into the preceding paragraph over adding a new mini-section or leaving an underfilled block.
- Do not overuse a single subject term such as `平台`. When the meaning stays the same, vary references naturally across `医标智绘`、`本作品`、`系统`、`该协作平台` and similar expressions, but keep the referent clear.
- If the project has two members or clear module ownership, make the module boundaries and interface boundaries visible enough to support later evaluation.
- Do not let `测试报告` degrade into a pile of weak tables. When measured data and修正记录 are available, weave them into natural prose so the section reads like real engineering validation.
- `测试报告` can still include one compact summary table or figure when that improves readability, but the section should not collapse back into table stacking.
- When writing `安装及使用`, first decide whose perspective the template expects. If the document is introducing a delivered platform to judges or end users, default to browser access, login entry, and typical operation flow rather than developer deployment commands such as Python or pip installation.
- Only describe repository-level commands, dependencies, and paths in `安装及使用` when the template clearly expects deployment guidance. Otherwise, keep those details behind the scenes and present a user-facing usage path.
- Even when installation content is derived from the repository, the wording should still sound like the project team submitting the work, not like an assistant explaining what the repository contains.
- Under strict page limits, chapters 4 to 6 should usually be strengthened by improving perspective and information density, not by simply adding length. A compact metrics figure in `测试报告`, a user-side flow table in `安装及使用`, and one synthesis table in `项目总结` are often better than longer prose blocks.
- When the later chapters feel visually thin, supplement them with screenshots from the real running system, such as actual page renders, logged-in interfaces, and startup terminal captures, instead of leaving the back half of the document as pure text.
- If a terminal screenshot is used, crop it to the meaningful runtime output region so window chrome, stray side panels, or unrelated console noise do not weaken the delivery.
- Make sure the structural order remains correct after automated insertion. Headings such as `第七章 参考文献` must appear before their entries rather than being stranded after them.
- If the document style expects each main chapter to begin on a new page, add page breaks deliberately and then re-compact the previous chapter so it does not leave an orphan line or a large blank block at the bottom.
- If justified paragraphs contain long English commands or identifiers and produce ugly broken spacing, split the sentence or move the command to its own line instead of forcing the paragraph to carry everything.
- Final delivery quality includes the opening state in Word. Turn off track-revision behavior and hidden markup views when the template accidentally leaves the document opening in a review-oriented state.

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
