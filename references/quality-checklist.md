# Quality Checklist

Run this checklist before treating a contest document as ready.

## Fit To Contest Template

- The chapter names match the contest or teacher template exactly.
- Each chapter answers the local prompt instead of drifting into generic SRS wording.
- The document feels like a competition submission, not an enterprise specification dump.
- If the organizer has explicit formatting rules, those rules override older default formatting preferences and are reflected in the final docx and PDF.
- If the organizer specifies `正文宋体、标题黑体` or a similar pure-font hierarchy, the final visible runs in Word actually reflect that hierarchy instead of preserving an older mixed-font convention.

## Content Quality

- Background and significance are concrete and tied to the project.
- Target users, scope, and core functions are explicit.
- Overview design shows module decomposition and relationships clearly.
- Overview design is not underwritten; it surfaces the real high-level technical focus with enough figure-table-text support.
- Detailed design includes real workflows, data design, and technical highlights.
- Test content shows evidence, not only conclusions.
- Installation and usage steps are short but executable.
- Project summary contains engineering reflection and evolution, not generic feelings.

## Rigor

- Claims about performance, security, reliability, or usability are measurable.
- Major technologies are justified in context.
- The AI or algorithm module has clear boundaries, inputs, outputs, and failure handling.
- If the project uses sensitive data, privacy and permission handling are visible.
- The tables, numbering, and terminology stay consistent throughout the document.

## Presentation

- Figures and tables are readable and actually support the argument.
- Figures preferably come from the user's real source materials when good source visuals are available.
- Any generated diagram keeps labels inside shapes and avoids chaotic arrow routing.
- Figure and table captions are placed below the object.
- The body text explicitly references visuals with phrases such as `如图x-x所示` or `如表x-x所示`.
- The visible main chapter title is a single consistent unit: the `第一章` prefix and the chapter name use the same Songti sizing and weight instead of looking like two mismatched layers.
- Table column widths are assigned by content density instead of being left at uniform default widths.
- Tables that still look tall have also been compacted through wording, internal margins, and paragraph spacing rather than only by dragging column widths.
- Page-constrained tables are kept as intact as possible, and table captions are not casually pushed onto the next page.
- Paragraphs are concise and not overloaded with background theory.
- Large blank regions at the bottom of a page have been checked for hidden manual page breaks or keep-with-next residue from the template, not only for paragraph length.
- Process descriptions read like human-written technical prose rather than AI-style `1. 2. 3.` bullet chains.
- Summary paragraphs do not rely on stiff formulaic connector chains such as repeated `首先` / `然后` / `最后` or `一是` / `二是` / `三是`.
- Section endings do not sound like the writer is talking to the reader about the act of writing.
- The narrative voice sounds like the submitting team speaking for the project, not like an AI or reviewer summarizing source materials.
- Chinese prose does not contain unnecessary spaces next to adjacent English, numbers, or symbols.
- Diagrams use consistent labels with the text.
- Screenshots reflect the real system instead of placeholder mockups when possible.
- Main chapter titles follow the template's centered style, while internal hierarchical headings are kept left aligned and restrained to a sensible depth.
- If the local template or user expects numbered main chapters, the final document actually uses titles such as `第一章 需求分析`, `第二章 概要设计`, and so on.
- `需求分析` does not stop after listing subheadings and tables; it ends with a short concluding paragraph that gathers the chapter argument.
- `概要设计` is not just one architecture diagram plus one module table when richer source screenshots exist.
- When the platform's key value lies in the workbench itself, the chapter shows the workbench in enough states or scales to make the interaction concrete.
- Newer quarterly or milestone reports have been checked for updated functions, interfaces, or deployment constraints, and those updates are not accidentally lost behind older polished material.
- Rendered pages do not contain obviously awkward short wrap lines where only one or two Chinese characters, or a tiny caption fragment, are stranded on the next line.
- When a page budget is tight, short concluding thoughts are folded into the surrounding paragraph instead of being turned into thin standalone blocks.
- If a short summary paragraph exists, it is merged naturally into the end of the chapter rather than being given an empty-feeling standalone `本章小结` heading.
- Repeated references to the project use varied but clear subjects instead of mechanically repeating `平台` in sentence after sentence.
- A chapter the user already considers acceptable has been migrated and reformatted carefully rather than rewritten into a weaker version.
- `测试报告` reads like measured validation and修正复盘, not like a stack of table shells.
- `测试报告` may include one compact summary table or figure, but prose remains the backbone and the layout does not regress into table stacking.
- `安装及使用` is grounded in the real code repository and usage docs instead of generic framework habits.
- `安装及使用` still sounds like the team presenting its own deployment path, not like an external narrator pointing at the repository.
- `第七章 参考文献` appears before the reference entries and is not separated from them by insertion-order mistakes.
- If each chapter starts on a new page, the previous page does not end with a single orphan line or an obviously oversized blank area that should have been compressed away.
- Word opens in a normal reading/printing state rather than exposing leftover review markup settings from the template.
- If Word should display `宋体/黑体`, the reopened style definitions and visible runs have been checked for theme-font residue instead of assuming the font alias issue will fix itself.
- Tables still show clear visible grid lines after PDF export rather than relying on a border style that disappears in rendering.
- Later chapters are not visually starved; if the real project can be launched, runtime screenshots or terminal captures have been considered for installation, usage, or validation sections.

## Final Delivery

- No placeholder text, unfinished bullets, or TODO markers remain.
- Chinese text was written through a UTF-8-safe path and not through shell-embedded non-ASCII snippets that can be downgraded to `?`.
- Reopen the generated `.docx` and sample-read the newly inserted paragraphs and table cells to confirm there is no mojibake, `????`, or mass question-mark replacement.
- The `.docx` version has clean styles, spacing, and pagination.
- User-specified formatting constraints such as Song font for Chinese, Times New Roman for English and numbers, first-line indent, paragraph spacing, and justification are actually applied where requested.
- The PDF render has no clipped text, broken tables, or unreadable images.
- References are in a consistent format.

## Common Failure Signals

If any of these are true, the document still needs work:

- the report sounds like a generated PRD with Chinese headings pasted on top
- Chinese content in the final docx or PDF appears as `?`, `????`, or visibly garbled text
- figure captions are above the image or table even though the user or source documents use below-caption style
- the prose repeatedly falls back to AI-looking numbered flow bullets instead of natural connected explanation
- the text sounds like an external assistant reporting on documents instead of the team presenting its own project
- the overview section looks thin, generic, or unsupported by visuals even though the source documents contain usable figures
- the chapter has layered headings but almost no substantive paragraphs under them
- the overview chapter contains architecture but barely any real platform interface evidence even though source screenshots are available
- an older baseline report was followed mechanically and newer quarterly progress was ignored
- the writing leans on repetitive connector formulas and sounds more like generated scaffolding than natural technical prose
- the closing paragraph sounds like the author is speaking to the reviewer about what the chapter just did
- the document keeps creating tiny standalone `本章小结` headings for one-sentence conclusions even under tight page limits
- a rendered page leaves one or two stray Chinese characters hanging on the next line and no one rewrote the sentence
- the chapter heading shows `第一章` in a visibly different font or size from the chapter name because template auto-numbering was left untouched
- a table is split across pages mainly because column widths stayed default and no one compacted the layout
- the table caption is stranded on the next page even though the table itself could have been compacted or moved as a whole
- a large blank region remains before a table or figure because a hidden template page break was left in place
- the design chapters have almost no diagrams
- the test section is mostly hollow tables with little narrative, metrics, or defect evidence
- the project summary repeats earlier chapters
- medical or AI claims are present but data handling and human review are absent
- the organizer's explicit font hierarchy is ignored because an older private formatting preference was followed instead
- the document claims to follow `宋体/黑体` organizer rules, but Word still shows `SimSun`-style leftovers or mixed western fonts because the runs were only half-updated
- the table style name says there should be borders, but the rendered PDF still looks borderless
- installation steps look plausible but cannot be traced back to the real repository, README, settings, or usage guide
- the back half of the report becomes text-only even though the running system could have supplied real screenshots
- a forced chapter page break leaves the previous page with a dangling last line or a large avoidable blank block
- Word opens with review markup turned on even though the final deliverable is meant for ordinary reading
