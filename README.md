# Exam Generator

A reusable AI agent skill for generating, reviewing, revising, and exporting reference exams from course materials.

Exam Generator provides a structured workflow for creating midterm exams, final exams, and standalone practice exams across different subjects and assessment formats. The skill uses the provided course materials to determine scope, structure, content, and course-specific difficulty rather than relying on a fixed exam template.

## What This Skill Does

Exam Generator supports four main tasks:

- **Generate** — create a midterm, final, or practice exam from the provided course materials.
- **Review** — validate an exam for correctness, scope, difficulty, structure, answer quality, and consistency.
- **Revise** — correct verified issues while preserving the intended structure and difficulty profile.
- **Export** — convert a finalized Markdown exam into a formatted PDF without changing its academic content.

## Supported Inputs

The skill can work with:

- Markdown or plain-text files **(preferred when available to reduce processing overhead and resource usage)**
- PDFs
- Images
- Lecture notes and course materials
- Exercises and question banks
- Previous or reference exams

Multiple source types can be used together when needed.

## Workflow

The typical workflow is:

`Generate → Review → Revise → Export`

Each stage is independent. A stage can be used directly when its required inputs are already available, so running the complete workflow is not required for every task.

Generation produces both the exam and a compact context file containing the decisions and source information needed by later stages.

## Difficulty Levels

Exam difficulty is specified using a five-level scale:

| Level | General meaning |
| --- | --- |
| **1** | Baseline or reference difficulty |
| **2** | Slightly more demanding |
| **3** | Clearly more demanding |
| **4** | High difficulty with substantial multi-step reasoning |
| **5** | Maximum discrimination within the defined course scope |

The scale is recalibrated for every course and source set. A level therefore describes the difficulty profile of the current exam rather than an absolute difficulty shared across different subjects.

When a reference exam is available, Level 1 is calibrated against that exam. When no reference exam is available, Level 1 represents the expected baseline of the requested assessment or practice set based on the available course materials, scope, and conditions.

See [`references/generate.md`](references/generate.md) for the full calibration rules.

## Usage

Example prompts:

**Generate**

> Generate a level 3 practice exam with 25 multiple-choice questions from the attached materials.

**Review**

> Review the exam.

**Revise**

> Revise the exam.

**Export**

> Export the exam to PDF.

## Repository Structure

```text
exam-generator/
├── README.md
├── LICENSE
├── SKILL.md                 # Main skill instructions and workflow routing
└── references/
    ├── sources.md           # Source selection and scope rules
    ├── generate.md          # Exam generation and difficulty calibration
    ├── review.md            # Review and validation
    ├── revise.md            # Revision workflow
    └── export-pdf.md        # PDF rendering and layout
```

## PDF Export

PDF export preferably uses **LuaLaTeX** or **XeLaTeX** for reliable Unicode, mathematical typesetting, font handling, figures, tables, and page layout.

The original development environment uses **TeX Live 2026** installed at:

```text
D:\texlive\2026
```

This location is treated as a preferred local setup, not as a required installation path.

If it is unavailable, the skill will attempt to use an existing `lualatex` or `xelatex` installation available through the system environment, or another compatible TeX Live or MiKTeX installation.

When no suitable TeX engine is available, another existing document/PDF renderer may be used only if it can preserve the required Unicode text, mathematics, fonts, figures, tables, and layout with comparable fidelity.

The skill should not silently install additional software. If no suitable renderer is available, it should preserve the usable source and intermediate files and report that PDF export could not be completed.

For the complete export and layout rules, see [`references/export-pdf.md`](references/export-pdf.md).

## Language

The README and repository metadata are written in English, while the core skill instructions and reference documentation are intentionally maintained in Vietnamese for easier day-to-day development, maintenance, and use.

## License

This project is licensed under the MIT License. See [`LICENSE`](LICENSE) for details.
