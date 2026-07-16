#  Human Validation Annotations for VADER-Derived Severity Labels
This repository contains the component produced during the study:

1. **160-tweet human validation annotations** — `human_validation/`

---



## 1. Human validation annotations (`human_validation/`)

- `human_validation_160tweets.csv` — 160 tweets, each independently labeled
  by three human annotators on the same 0–3 severity scale used for the
  VADER-derived labels.
- `annotation_guidelines.md` — the exact instructions given to annotators
  (label definitions, tie-breaking rule, and independence protocol).

### File: `human_validation_160tweets.csv`

| Column | Description |
|---|---|
| `annot_id` | Unique row identifier (1–160) |
| `tweet_text` | Tweet text shown to annotators (one row has empty/deleted text, retained for completeness) |
| `annotator1_label` | Annotator 1's severity score (0 = Not-Offensive, 1 = Low, 2 = Mild, 3 = High) |
| `annotator2_label` | Annotator 2's severity score (0–3, same scale) |
| `annotator3_label` | Annotator 3's severity score (0–3, same scale) |

**Label scale** (full definitions in `annotation_guidelines.md`):

| Score | Label | Meaning |
|---|---|---|
| 0 | Not-Offensive | Nothing offensive at all |
| 1 | Low | Mildly rude/crude/sarcastic, not targeting anyone |
| 2 | Mild | Clearly offensive — insults or mocks a person/group, no slurs or threats |
| 3 | High | Severely offensive — slurs, hate speech, dehumanizing language, or threats |

Annotators were instructed to default to the higher score when uncertain,
score the text rather than their personal reaction, and label independently
without comparing notes until all annotations were complete.

---

## Source data

The tweets in this repository are a stratified sample drawn from the
Davidson et al. (2017) *Hate Speech and Offensive Language* dataset
(https://github.com/t-davidson/hate-speech-and-offensive-language),
licensed under the MIT License. The original license notice is preserved
below; our own annotations (all novel
material produced for this study) are released separately .

**Citation for the source data:**

> Davidson, T., Warmsley, D., Macy, M., & Weber, I. (2017). Automated Hate
> Speech Detection and the Problem of Offensive Language. *Proceedings of
> the 11th International AAAI Conference on Web and Social Media (ICWSM)*,
> 512–515.

---

## Repository structure

```
.
├── README.md
├── LICENSE.md
└── human_validation/
    ├── human_validation_160tweets.csv
    └── annotation_guidelines.md
```
