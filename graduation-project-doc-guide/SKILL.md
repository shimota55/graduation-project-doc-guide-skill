---
name: graduation-project-doc-guide
description: Rules for writing, formatting, structuring, and reviewing graduation project (مشروع التخرج) documentation according to the Programming Technologies Department (قسم تقنيات البرمجة), College of Computer Technology – Tripoli, Libya (Documentation Guide, 3rd edition, 2014, by Dr. Aqeel Mohammed Aqeel). Use this skill whenever the user mentions graduation project documentation, final project report, دليل توثيق مشاريع التخرج, توثيق المشروع, تقرير مشروع التخرج, a thesis-style report for the College of Computer Technology Tripoli, or asks to format, outline, check, or draft a title page, table of contents, list of tables/figures, abbreviations list, references list, or appendices for a graduation project, even if they do not name the guide explicitly. Also use it when generating a Word/PDF graduation report that must follow department formatting (margins, fonts, numbering, headers/footers).
---

# Graduation Project Documentation Guide (DPT, 3rd edition, 2014)

This skill encodes the official documentation guide of the Programming Technologies Department, College of Computer Technology – Tripoli (Ministry of Higher Education and Scientific Research). The department does not accept or allow a project to be defended until the documentation conforms to these rules, and the student is responsible for conformity. So when helping a student, be exact: small deviations (wrong margin, wrong heading size, wrong numbering) are exactly what reviewers reject.

## How to use this skill

Decide which of these the user needs, then read only the matching reference file:

| User need | Read |
|---|---|
| Formatting a document (fonts, margins, spacing, numbering, headers, tables/figures captions, abbreviations, equations, printing/binding) | `references/formatting-spec.md` |
| What parts the document must contain and what goes in each (title page, abstract, TOC, lists, chapters, references, appendices) | `references/document-structure.md` |
| Writing the references list or citing sources | `references/references-format.md` |
| Ready-made templates: title page, sample table of contents for a project | `references/templates.md` |
| Reviewing an existing draft | Use the checklist below, then consult the reference files for any item that fails |

## Quick facts (memorize these; details are in the references)

- Paper: plain white A4, no colored/decorated ready-made cover sheets.
- Minimum length: **80 pages** of project body (front matter, lists, references, appendices do not count toward the 80, but the chapter-cover page is counted in numbering without printing its number).
- Language: Arabic **or** English, but one language for the entire document.
- Font: **Times New Roman** (the department's original guide specifies Arabic Transparent; the user has chosen Times New Roman instead, so use it unless they say otherwise). Headings 1 to 5 sizes are 18 / 16 / 14 / 12 / 12 pt; body text 12 pt.
- Line spacing 1.5, with automatic space after each paragraph; text justified.
- Margins (Arabic text): top 2.5 cm, bottom 2.5 cm, right 4 cm, left 2 cm. For English text, swap right and left (left 4 cm, right 2 cm).
- Header: chapter title on the left, chapter number on the right (Arabic layout). Footer: page number only, centered, no symbols.
- Front matter pages are numbered with Roman numerals; the body is numbered 1, 2, 3, … starting from the first chapter's cover page (counted, not printed).
- Headings are numbered hierarchically (1.1, 1.2.3, max 4 levels). Tables and figures are numbered by chapter (Table 2.7, Figure 5.2).
- Deliver a PDF-convertible, word-processor-written file; convert to PDF after proofreading so fonts and layout stay fixed.

## Workflow

1. **Identify the language** the student is writing in (Arabic or English) and apply the matching margin/alignment rules. Reply and draft in the language the user writes in.
2. **Clarify only what is missing**: project title, student name(s) and enrollment number(s), supervisor name, academic year/semester, degree (Bachelor or Higher Diploma), and which parts exist already. Do not interrogate; ask for what is truly needed to fill a template, and use placeholders otherwise.
3. **Produce the deliverable**:
   - For a Word file, use the `docx` skill for the mechanics and apply the settings from `references/formatting-spec.md` (page size A4, margins, styles for Heading 1 to 5, line spacing, header/footer, section-based page numbering, right-to-left paragraphs for Arabic). Set Times New Roman for all four font slots (ascii, hAnsi, cs, eastAsia) so Arabic and Latin text both use it; it is installed on virtually every Word setup, so no fallback is needed.
   - For an outline or advice, answer in the chat using the structure in `references/document-structure.md`.
4. **Self-check** against the checklist below before presenting.

## Arabic (RTL) pitfalls when generating Word files

Marking only the text runs as right-to-left is not enough; Word then treats the paragraphs as left-to-right (wrong alignment, misplaced punctuation, mixed Latin terms jumbled). Set RTL at every level:

- Every paragraph (body, headings, captions, table cells, header/footer, even empty spacers) must be RTL. In docx-js the option is `bidirectional: true` on `Paragraph`; `bidi: true` is silently ignored. Also put it in the default paragraph style, plus `rightToLeft: true` on runs.
- Add `<w:bidi/>` to the section properties (`sectPr`) of `word/document.xml` after generating (docx-js has no option for it).
- Tables: `visuallyRightToLeft: true`, so the first column sits at the right.
- Header with chapter title (left) and chapter number (right): do not rely on tab stops in an RTL paragraph (the tab wraps to a second line). Use a borderless two-cell RTL table with a bottom rule: the first cell (right) holds the chapter number, the second (left) holds the chapter title.
- Write Latin terms (e.g. Database, GUI) as separate non-RTL runs inside the Arabic paragraph.
- Always render to PDF/PNG and look at it before presenting.

## Review checklist

Use this when the user shares a draft or asks "is this correct?". Report findings as a short list of concrete fixes (what is wrong, what the rule is, how to fix it); do not rewrite the whole document unless asked.

- Title is short, descriptive, objective.
- Single language throughout; scientific terms in Arabic text are followed by the English term in parentheses.
- Body ≥ 80 pages (excluding listed exceptions).
- Font and sizes per heading level; body 12 pt; emphasis (bold/italic) only on a word, phrase, or at most a whole paragraph or page, never stretched beyond that.
- 1.5 line spacing, justified, space added after each paragraph.
- Margins correct for the language.
- Header (chapter number + title) and footer (page number only) present; chapter pages begin on a new page.
- Front matter in Roman numerals, body in Arabic numerals, no decoration around the numbers; numbering continuous (not restarted per chapter).
- Heading numbers hierarchical and not deeper than 4 levels.
- Every table/figure has a chapter-based number and a short descriptive caption (tables: caption above; figures: caption below); the word "illustrates/يوضح" is not used inside captions; every one is referred to in the text.
- Abbreviations written in full at first use, in capital letters, and listed in the abbreviations list.
- Equations numbered sequentially at the right-hand margin.
- No large empty gaps except at the end of a chapter; tables that do not fit are split with a repeated header row and a "(continued)" note, and figures are resized to fit.
- References: numbered, correctly formatted by source type, cited in text with [n]; Arabic and English references in two separate sections when both exist.
- All required parts present and in the correct order (see `references/document-structure.md`).
- Appendices labeled A, B, … with pages A1, A2, ….

## Notes and known ambiguities in the source guide

- The guide says "Greek numbering" (الترقيم اليوناني) for front matter and shows examples like 5, 55, 555, IV; these are Roman numerals (i, ii, iii, iv…). Use Roman numerals.
- The sample table of contents in the guide is an illustration for a different project (an electronic school); adapt chapter titles to the student's project rather than copying them.
- Final copies are printed and bound (hard black cover) only **after** the defense and after the committee's corrections are made; copies given to the committee are not bound. The department head announces the number of copies required.
