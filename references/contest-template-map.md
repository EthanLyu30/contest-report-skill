# Contest Template Map

Use this file when drafting or revising any section of a Chinese university software competition design and development document.

## Primary Mapping

| Contest section | What it must answer | Strong borrowed sources | Recommended evidence |
|---|---|---|---|
| 需求分析 | Why build it, for whom, what main functions and performance matter, and how it compares to alternatives | SRS product scope and product functions, business analyst discovery, PRD goals and audience | short background paragraph, source screenshot or scene figure, user roles or scenario table, competitor comparison table |
| 概要设计 | What modules exist, how they relate, what interfaces connect them, and what the overall interaction path looks like | IEEE 1016 context, composition, interface viewpoints; architecture workflows | source architecture figure, module table, interface or interaction explanation in prose |
| 详细设计 | How representative pages, data structures, key workflows, and core algorithms actually work | design document templates, RAD and SDD structures, focused technical notes | UI screenshots, flowcharts, ER diagram, table schemas, algorithm flow, API examples |
| 测试报告 | What was tested, what failed, what was fixed, and what technical indicators were achieved | verification sections, traceability mindset, pragmatic QA writeups | representative test cases, before-after fixes, result table, performance or usability metrics |
| 安装及使用 | How to install, what environment is needed, and how to run a typical workflow | deployment notes and user manual fragments | environment table, install steps, default login or setup notes, typical use flow |
| 项目总结 | What was learned, what was hard, how work was divided, and how the project can evolve | course-style summary patterns, engineering retrospectives | workload highlights, challenge-resolution table, roadmap bullets |

## Local Template Constraints

Honor these defaults unless the user or a newer organizer template overrides them:

- If the organizer gives explicit document formatting rules, those rules override earlier house preferences for fonts, title hierarchy, or spacing
- If the organizer specifies a Chinese font hierarchy such as `正文宋体、标题黑体`, apply that hierarchy to Chinese runs while keeping English letters and numbers in `Times New Roman`, unless the organizer explicitly requires a pure single-font document

- `需求分析`: keep it compact but not skeletal; if the source materials already support stronger argumentation, it is better to add one more solid paragraph or summary than to leave the chapter hollow
- `概要设计`: prefer figures over long prose, but do not compress it so far that only one architecture figure and one module table remain; when the project has usable interface screenshots, let them share the load with the architecture view
- If the template recommends one to two pages, prefer denser combined figures and tighter tables before deleting concrete implementation evidence
- `详细设计`: emphasize interfaces, database design, key algorithms, technical highlights, and typical usage flows; avoid long unfocused exposition
- `测试报告`: keep it brief and evidence-driven
- `安装及使用`: keep installation environment and common workflow short and runnable
- `项目总结`: usually within 1 A4 page

## Section Tactics

### 需求分析

Use this structure:

1. one short paragraph on background and practical significance
2. one sentence on target users
3. one sentence on project positioning
4. one compact list or table for core functions
5. one compact competitor comparison if competitors exist
6. when a source document already has a strong demand-side image or screenshot, reuse it and reference it in the text before placing it
7. keep the speaker identity stable: write as the project team, not as an observer explaining what the documents say
8. do not stop at subheadings alone; give the chapter a closing paragraph that summarizes what the demand analysis proves and what it implies for later design
9. when the user expects numbered main chapters, render the chapter title as `第一章 需求分析` instead of a bare `需求分析`
10. if the chapter ending is only a short paragraph, do not force a separate `本章小结` subheading just for formality

Presentation rule:

- lead into visuals with sentences like `如图1-1所示` or `如表1-1所示`
- place figure and table captions below the object, not above it
- if a table or figure is forced onto the next page while the previous page still leaves a suspicious blank block, inspect and remove hidden template page breaks before continuing to cut text
- avoid robotic numbered bullets when prose can explain the logic more naturally
- avoid stiff connective formulas such as repeated `首先` / `然后` / `最后` or summary chains like `一是` / `二是` / `三是` when a smoother paragraph will read more like a real contest submission
- avoid chapter-ending lines that sound like the writer is talking to the reader about the writing process
- avoid meta-source wording such as `结合技术报告...` or `从商业计划书中可以看出...`
- do not leave extra spaces between Chinese and adjacent English, numbers, or symbols in the final Chinese prose
- treat the chapter title as centered if the template does so, but keep internal subheadings left aligned; prefer two-level headings unless the content truly needs a third level
- vary the subject naming naturally; do not repeat `平台` in every sentence when `医标智绘`、`系统`、`本作品` or `该协作平台` would read better
- if the chapter will end before the next main chapter starts on a new page, re-compact the chapter so the previous page does not end with a single dangling line or a large avoidable blank block

Avoid:

- writing a long textbook introduction
- listing implementation details too early
- claiming innovation without a concrete point of comparison

### 概要设计

Use this structure:

1. system decomposition into 4 to 8 modules
2. one diagram showing module relationships
3. one diagram or table showing main interfaces or interaction flow
4. one short explanation of why this decomposition fits the project
5. if the project has already produced platform screenshots, architecture figures, WSI annotation views, task pages, or data-path figures, use them to show the key technical focus instead of relying on one thin paragraph
6. when the workbench is central to the project, show the workbench from more than one scale or state if the source documents support it, such as full-slice view, local refinement view, and result view
7. when both an older polished report and a newer quarterly report exist, keep the older report as the wording baseline but let the newer report update the actual implemented functions and current interface state

Presentation rule:

- prefer source architecture or workflow figures over freshly generated ones when the source figure is already readable
- if the workflow is written in text, explain it as a connected process paragraph instead of `1. 2. 3.` bullet fragments
- place figure and table captions below the object and cite them in the paragraph immediately before or after
- keep the overview section rich enough to show the real highlights: architecture, key data path, module split, and at least one clear interaction or interface clue when the materials support it
- when the chapter is still too thin but the page budget is tight, prefer one compact synthesis paragraph that ties modules, call flow, and interface transitions together over opening another weak subsection
- do not let `概要设计` become architecture-only; if real platform screenshots exist, they should usually appear in this chapter
- if space is tight but several screenshots are all important, merge them into one clean combined figure rather than dropping the newer interfaces
- do not reuse the exact same screenshot in multiple later chapters unless the comparison itself is the point; if an interface must recur, switch to a different crop, state, or companion screen so each figure carries distinct information
- after layout is rendered, scan for ugly wrap behavior; if a caption or paragraph leaves only one or two Chinese characters on a new line, rewrite the sentence or shorten the caption
- if the chapter ends with only a brief收束段, merge it into the end of the section instead of adding a standalone `本章小结` heading

Avoid:

- only writing text with no figure
- writing the section as if an assistant is reporting back on source files
- mixing low-level table fields into the high-level section
- drawing a diagram with no explanation of information flow

### 详细设计

Prioritize these items:

- representative UI pages and key interaction steps
- database tables or entity relationships if the project stores data
- workflow logic for upload, annotation, review, export, or core user tasks
- key algorithms, model-assisted steps, or technical innovations
- if the user already has a later draft chapter they consider acceptable, migrate its good structure and screenshots before deciding to rewrite anything

Avoid:

- dumping every page screenshot with no commentary
- listing every database field if only a few matter
- describing the framework stack without connecting it to the workflow

### 测试报告

A strong compact test section usually includes:

- 3 to 6 representative test cases
- at least one bug or defect and how it was corrected
- measurable results carried by prose, with tables used only when they genuinely clarify rather than bloat the section
- at most one compact summary table or figure when it improves scanability without taking over the section
- one compact synthesis of performance, compatibility, and修正效果 when the template page budget is tight

Avoid:

- explaining what unit testing means
- giving only "all tests passed"
- ignoring negative or exception cases
- stacking multiple generic tables when the same evidence would read more naturally in paragraph form

### 安装及使用

Include:

- environment requirements
- deployment or startup steps
- default usage path
- one typical scenario from login to result output
- repository-backed commands, directories, and feature usage notes drawn from the real codebase, README, settings, or usage documents
- when possible, include screenshots from the real running project, such as the landing page, login page, workbench, or startup terminal, so the section documents an actual executable state rather than a purely textual setup path
- wording that still sounds like the submitting team documenting its own system rather than an assistant describing repository contents
- final prose should describe the system directly and must not explain the writing choice itself with sentences like `为了让用户侧说明更贴近真实操作...` or `结合某报告材料可以看出...`

Avoid:

- giant environment dumps
- repeating testing content
- omitting browser, database, GPU, or model dependency requirements when they matter
- inventing steps that cannot be traced back to the real project repository
- leaving long command names inside justified prose when moving them to a separate command line would read cleaner

### 项目总结

Good summary themes:

- key coordination and task decomposition choices
- hardest engineering problems and how they were solved
- what improved in the team's technical ability
- practical next-step evolution

Avoid:

- generic gratitude statements
- pure marketing language
- repeating the introduction section

## References

- If the document keeps a dedicated `参考文献` chapter, add in-text citations in the正文 where the referenced method, model, or conclusion is actually invoked.
- In Chinese contest prose, citations can be placed at the end of the relevant sentence immediately before the punctuation, for example `……取得了更稳定的结果[1-3]。`
