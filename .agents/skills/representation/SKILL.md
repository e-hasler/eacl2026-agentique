---
name: representation
description: Explains how to choose a representative sample of annotated data
---

## Representation

A sample is representative when it reflects the main annotation patterns in the source data. 

Select rows using these priorities:
1. Include at least one instance of every possible POS value.
2. Keep roughly the same ratio of POS values as in the source data, while giving priority to including every POS at least once.
3. Keep roughly the same ratio of simple and compound POS compositions as in the source data.
4. Include different word forms and lemmas for frequent POS values, rather than repeating the same examples.
5. Preserve complete source rows and select only the requested number of rows.

## Priority order

If the requested sample is too small to satisfy every condition, prioritize POS coverage, then POS ratios, then composition ratios.
