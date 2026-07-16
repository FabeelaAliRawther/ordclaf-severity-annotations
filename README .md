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

The tweets in the human validation set are drawn from the TweetEval 
benchmark's Offensive Language split (Barbieri et al., 2020), which is 
itself built on the OLID dataset (Zampieri et al., 2019).

Citation:
> Barbieri, F., Camacho-Collados, J., Espinosa-Anke, L., & Neves, L. (2020). 
> TweetEval: Unified Benchmark and Comparative Evaluation for Tweet 
> Classification. Findings of EMNLP 2020, 1644–1650.

> Zampieri, M., Malmasi, S., Nakov, P., Rosenthal, S., Farra, N., & 
> Kumar, R. (2019). Predicting the Type and Target of Offensive Posts in 
> Social Media. Proceedings of NAACL-HLT 2019, 1415–1420.
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
