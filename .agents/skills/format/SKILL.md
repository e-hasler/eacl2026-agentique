---
name: format
description: Explains the expected format of .tsv files
---

## Format of .tsv files

A TSV file uses one row per line and one tab between columns. The first row is the header.
For annotation files, use the columns `text_form`, `form`, `lemma`, and `pos` in this order.

## Allowed characters

The allowed POS tokens are strictly:
`A`, `DET`, `DET@A`, `I+Adv`, `I+AdvPr`, `I+Conj`, `I+Neg`, `I+Part`, `I+Part@I+Adv`, `I+Prep`, `N+Ant`, `N+Com`, `N+Com+eTurc`, `N+Top`, `PRO+Dem`, `PRO+Ind`, `PRO+Per1p`, `PRO+Per1s`, `PRO+Per2p`, `PRO+Pos1p`, `PRO+Pos1s`, `PRO+Rec`, `PRO+Ref1s`, `PRO+Ref3s`, `PRO+Rel`, and `V`.

## Rules

- Keep the number and order of columns identical in every row.
- Do not replace tabs with spaces or commas.
- Preserve the spelling, accents, and diacritics of the data.
- Do not add spaces before or after a field.
- Input samples may have empty `lemma` and `pos` fields; completed annotations may not.
- Use strictly one of the allowed POS tokens above; do not invent, normalize, or replace a token with a synonym.
- Do not add, remove, or reorder rows.

## Ambiguous cases

- An empty field is valid only when the instructions explicitly allow it.
- A tab inside a field is not valid; it must separate columns.
- A missing or extra column makes the row invalid.
- Keep compound POS labels exactly as they appear in the reference data, for example `I+Adv` or `DET@A`.
