# Project
Evaluate the ability of a sub-agent to associate the correct lemma and POS with a list of Ancient Greek words in unseen data, based on a training sample.

## Structure
```text
data/corpus/
├── test_in-domain/GRC_test.tsv  # Annotated source data and reference labels
└── grc_sample.tsv               # Sample to annotate
results/
├── grc_sample.tsv               # Agent annotations
└── incorrect_grc_sample.tsv     # Incorrect annotations
```

## Method and delegation
Follow this method:
1. Ask the agent sampler.toml to extract a representative subset from data/corpus/test_in-domain/GRC_test.tsv removing the annotations of POS and lemma and save it to data/corpus/grc_sample.tsv.
2. Ask the agent tester.toml to create tests to evaluate the code of the future annotator.
3. Ask the agent annotator.toml to associate the correct POS and lemma with the data in data/corpus/grc_sample.tsv, based on the training sample and without using the reference labels in data/corpus/test_in-domain/GRC_test.tsv, and put the results in results/grc_sample.tsv.
4. Run the tests and put the incorrect sample in results/incorrect_grc_sample.tsv.

## Prohibited
You are not allowed to access or modify any file that I did not mention above. In particular, you are only allowed to access the following files:
```
data/corpus/test_in-domain/GRC_test.tsv
data/corpus/grc_sample.tsv
results/grc_sample.tsv
results/incorrect_grc_sample.tsv
```