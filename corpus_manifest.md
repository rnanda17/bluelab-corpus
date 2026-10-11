# Corpus manifest — bottom-up taxonomy test

Nine legal instruments in clean markdown, assembled for a legal-informatics
analysis of ABS / MGR relations plus deliberate cross-domain tension. Original
source files are kept in `source_pdfs/` for provenance.

**Provenance key:** *Supplied* = clean markdown provided by Henrique (not
touched in this step). *Fetched* = downloaded from an authoritative source and
converted in this step.

| # | File | Instrument | Scope | Provenance | Source file |
|---|------|-----------|-------|-----------|-------------|
| 1 | `cbd.md` | Convention on Biological Diversity | Full text + annexes (as supplied) | **Supplied** | `source_pdfs/cbd.pdf` |
| 2 | `nagoya.md` | Nagoya Protocol on ABS (to the CBD) | Full text (as supplied) | **Supplied** | `source_pdfs/nagoya.pdf` |
| 3 | `bbnj.md` | BBNJ Agreement (2023 High Seas Treaty) | Full text (as supplied) | **Supplied** | `source_pdfs/bbnj.pdf` |
| 4 | `eu511.md` | Regulation (EU) No 511/2014 (Nagoya user-compliance) | Full text (as supplied) | **Supplied** | `source_pdfs/eu-511-2014.pdf` |
| 5 | `itpgrfa.md` | International Treaty on Plant Genetic Resources for Food and Agriculture | **Extract** — Art. 2 (definitions) + Part IV, Arts. 10–13 | **Fetched** (FAO) | `source_pdfs/itpgrfa.pdf` |
| 6 | `gratk.md` | WIPO Treaty on IP, Genetic Resources and Associated Traditional Knowledge | Full text (preamble + Arts. 1–22 + footnotes) | **Fetched** (WIPO) | `source_pdfs/gratk.pdf` |
| 7 | `unclos.md` | UN Convention on the Law of the Sea | **Extract** — Art. 1 + Part XI + Part XII + Part XIII | **Fetched** (UN DOALOS) | `source_pdfs/unclos.pdf` |
| 8 | `trips.md` | Agreement on Trade-Related Aspects of Intellectual Property Rights | **Extract** — Arts. 1, 27, 29 (+ definitional footnotes) | **Fetched** (WTO) | `source_pdfs/trips.pdf` |
| 9 | `eu2015_1866.md` | Commission Implementing Regulation (EU) 2015/1866 | Full text (Arts. 1–13 + Annexes I–IV) | **Fetched** (EUR-Lex) | `source_pdfs/eu-2015-1866.pdf` |

## Scope detail (included / omitted) for the fetched instruments

- **`itpgrfa.md`** — *Included:* Article 2 (Use of terms — the definitions, from
  Part I) and the whole of Part IV (Articles 10–13, the Multilateral System of
  Access and Benefit-sharing). *Omitted:* Articles 1, 3–9 and 14–35, the two
  Annexes, and the preamble; also the FAO booklet's photographs and captions.
- **`gratk.md`** — *Included:* full treaty (preamble + Articles 1–22). Footnotes
  (including the Agreed Statements) are collected in a "Footnotes" section at the
  end. *Omitted:* the WIPO-added Table of Contents, which the original marks as
  not forming part of the Treaty text.
- **`unclos.md`** — *Included:* Article 1 (Use of terms and scope) and the
  complete Part XI (The Area, Arts. 133–191), Part XII (Protection and
  Preservation of the Marine Environment, Arts. 192–237) and Part XIII (Marine
  Scientific Research, Arts. 238–265), with all their Sections and Subsections.
  *Omitted:* the Preamble, Parts II–X and XIV–XVII, the Final Provisions, and the
  nine Annexes.
- **`trips.md`** — *Included:* Article 1 (with its definitional footnotes 1–2),
  Article 27 and Article 29, plus the Part/Section headings that locate them.
  TRIPS has no standalone definitions article; its operative definitions
  ("intellectual property", "nationals", the convention short-titles, "WTO
  Agreement") are in Article 1 and footnotes 1–2, which are included. *Omitted:*
  all other provisions (Articles 2–26, 28, 30–73 and their Parts/Sections).
- **`eu2015_1866.md`** — *Included:* full regulation — title, preamble
  (citations + recitals 1–14), Articles 1–13, and Annexes I–IV. The Annexes are
  tabular model forms; their text is transcribed verbatim in reading order but
  the original grid layout is approximated (see the note in that file).

## Sources (authoritative)

| Instrument | Authority | URL |
|-----------|-----------|-----|
| ITPGRFA | FAO | `https://www.fao.org/3/i0510e/i0510e.pdf` |
| GRATK | WIPO Lex (TRT/GRATK/001) | `https://www.wipo.int/wipolex/en/treaties/textdetails/19849` |
| UNCLOS | UN DOALOS | `https://www.un.org/depts/los/convention_agreements/texts/unclos/unclos_e.pdf` |
| TRIPS | WTO | `https://www.wto.org/english/docs_e/legal_e/27-trips.pdf` |
| EU 2015/1866 | EUR-Lex (CELEX 32015R1866) | `https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32015R1866` |

## Conversion method & fidelity (fetched instruments)

- Text extracted from the official PDFs; page headers/footers/numbers and photo
  captions removed; hard line-wraps rejoined; words broken across line breaks
  de-hyphenated; typographic ligatures repaired; footnotes relocated to a
  "Footnotes" section. Article/paragraph numbering is preserved verbatim.
- Each converted file passed a **character-level check**: the alphanumeric stream
  of the output was compared against the source's, so any added, dropped or
  altered word fails the check. All five passed exactly.
- **One deliberate correction (UNCLOS):** the official PDF font-encodes the digit
  "1" as the letter "l" in several numeric cross-references (e.g. "paragraph l" →
  "paragraph 1"; "article l4" → "article 14"). These 7 instances were corrected;
  genuine subparagraph *letter* references such as "(l)" and "paragraph 2(l)" are
  preserved as-is.

## Note for the later (blind) relation-discovery run

Two relations in this corpus are **real but not textually explicit**. A
text-only pass may surface them as only thematically linked — that is an expected
result, not a coverage failure:

1. **TRIPS ↔ GRATK (patent disclosure).** Whether a mandatory disclosure
   requirement is compatible with TRIPS patent rules lives largely in negotiating
   history and WTO/WIPO politics; the provisions do not cite each other.
2. **GRATK disclosure ↔ Nagoya/CBD ABS duties.** Parallel obligations across
   different legal domains (patent law vs ABS) pointing at the same underlying
   genetic resources.
