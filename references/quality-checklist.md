# Quality Checklist

Run this checklist before treating a contest document as ready.

## Fit To Contest Template

- The chapter names match the contest or teacher template exactly.
- Each chapter answers the local prompt instead of drifting into generic SRS wording.
- The document feels like a competition submission, not an enterprise specification dump.

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
- Paragraphs are concise and not overloaded with background theory.
- Process descriptions read like human-written technical prose rather than AI-style `1. 2. 3.` bullet chains.
- The narrative voice sounds like the submitting team speaking for the project, not like an AI or reviewer summarizing source materials.
- Chinese prose does not contain unnecessary spaces next to adjacent English, numbers, or symbols.
- Diagrams use consistent labels with the text.
- Screenshots reflect the real system instead of placeholder mockups when possible.
- Main chapter titles follow the template's centered style, while internal hierarchical headings are kept left aligned and restrained to a sensible depth.
- `需求分析` does not stop after listing subheadings and tables; it ends with a short concluding paragraph that gathers the chapter argument.
- `概要设计` is not just one architecture diagram plus one module table when richer source screenshots exist.
- When the platform's key value lies in the workbench itself, the chapter shows the workbench in enough states or scales to make the interaction concrete.

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
- the design chapters have almost no diagrams
- the test section has no metrics or defect evidence
- the project summary repeats earlier chapters
- medical or AI claims are present but data handling and human review are absent
