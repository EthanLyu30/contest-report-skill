# Source Stack

Use this file to decide which outside method or template to borrow from without letting the contest document become bloated.

## Hard Outer Shell

Always follow these first:

- local contest docx template
- local submission requirements
- teacher or organizer naming and length expectations

## Requirement Precision

Borrow from software requirement templates when you need:

- sharper functional boundaries
- measurable non-functional requirements
- interface and verification clarity

Good fit:

- `jam01/SRS-Template`
- IEEE 830 style SRS templates

In real contest work, product briefs and business plans are often the best source for:

- project background and practical significance
- target users and usage scenarios
- competitor comparison
- platform positioning and value expression

## Design Precision

Borrow from software design document templates when you need:

- clearer module decomposition
- interface viewpoints
- data architecture and subsystem explanation

Good fit:

- IEEE 1016 style design templates
- `Xett/Software-Design-Documentation`
- `MarkdownSoftwareEngineering`

In real contest work, technical reports and progress or quarterly reports are often the best source for:

- actual module boundaries already implemented
- real workflow details
- model names, data flow, and export paths
- deployment constraints and engineering bottlenecks

Prefer these implementation-grounded materials over commercial pitch wording when drafting 概要设计 or 详细设计.

## Discovery And Planning Logic

Borrow from BA, PM, and architect style workflows when you need:

- better problem framing
- stronger user and competitor analysis
- cleaner requirement prioritization
- more justified architecture choices

Good fit:

- BMAD style business analyst, product manager, and system architect flows

## Security And Traceability Add-Ons

Use these only when the project or the user needs them:

- security and privacy explanation for sensitive data
- requirement-test linkage
- structured quality checks

Good fit:

- `security-threat-model`
- traceability or spec lint tools

## Compression Rule

The contest document should absorb the strengths of these sources, not mirror their full chapter structures.

If a borrowed framework adds too much ceremony, compress it into:

- one table
- one figure
- one short subsection
- or one sentence with a measurable indicator
