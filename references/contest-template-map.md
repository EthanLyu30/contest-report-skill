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

- `需求分析`: suggested to stay within 1000 Chinese characters, preferably within about 300 characters plus a compact table when possible
- `概要设计`: prefer figures over long prose; keep the overall section around 1 page and usually no more than 2 A4 pages
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

Presentation rule:

- lead into visuals with sentences like `如图1-1所示` or `如表1-1所示`
- place figure and table captions below the object, not above it
- avoid robotic numbered bullets when prose can explain the logic more naturally
- avoid meta-source wording such as `结合技术报告...` or `从商业计划书中可以看出...`
- do not leave extra spaces between Chinese and adjacent English, numbers, or symbols in the final Chinese prose

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
5. if the project has already produced platform screenshots, architecture figures, or data-path figures, use them to show the key technical focus instead of relying on one thin paragraph

Presentation rule:

- prefer source architecture or workflow figures over freshly generated ones when the source figure is already readable
- if the workflow is written in text, explain it as a connected process paragraph instead of `1. 2. 3.` bullet fragments
- place figure and table captions below the object and cite them in the paragraph immediately before or after
- keep the overview section rich enough to show the real highlights: architecture, key data path, module split, and at least one clear interaction or interface clue when the materials support it

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

Avoid:

- dumping every page screenshot with no commentary
- listing every database field if only a few matter
- describing the framework stack without connecting it to the workflow

### 测试报告

A strong compact test section usually includes:

- 3 to 6 representative test cases
- at least one bug or defect and how it was corrected
- one result table for performance, availability, usability, or deployment convenience

Avoid:

- explaining what unit testing means
- giving only "all tests passed"
- ignoring negative or exception cases

### 安装及使用

Include:

- environment requirements
- deployment or startup steps
- default usage path
- one typical scenario from login to result output

Avoid:

- giant environment dumps
- repeating testing content
- omitting browser, database, GPU, or model dependency requirements when they matter

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
