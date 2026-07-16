# Human Validation Annotation Guidelines

These are the instructions given to human annotators for the 160-tweet human
validation set used to check agreement against the VADER-derived four-class
severity labels (Section 5.2 of the paper).

## Task

Read each tweet. Decide how offensive it is. Assign one score (0, 1, 2, or 3).

## Label scale

| Score | Label | Definition | Example pattern |
|---|---|---|---|
| 0 | Not-Offensive | Nothing offensive at all — a normal tweet | Everyday content, jokes, complaints about weather/traffic, etc. |
| 1 | Low | Mildly rude, crude, sarcastic, or irritated, but not really attacking anyone | Swearing out of frustration, sarcasm, mild complaining, edgy humor with no real target |
| 2 | Mild | Clearly offensive — insulting or mocking a person or group by name-calling or derogatory language, but no slurs or threats | "You're an idiot," mocking someone's appearance/intelligence, group stereotyping without slurs |
| 3 | High | Severely offensive — slurs, hate speech, dehumanizing language, threats, or telling someone to hurt themselves/others | Racial/ethnic/gender slurs, explicit threats, "kill yourself," dehumanizing a group |

## Annotation rules

1. **If stuck between two scores, pick the higher one.** Don't agonize — err toward the more severe label when genuinely unsure.
2. **Judge the words, not your personal reaction.** A tweet may be unfunny or annoying without being offensive — score strictly against the definitions above, not personal taste.
3. **Don't skip any rows, and don't discuss with the other annotator until both of you are completely done.** Comparing notes partway through invalidates the independent-agreement measurement that this exercise is designed to produce.

## Annotators

Three annotators independently labeled all 160 tweets under the above protocol.
Their labels are recorded as `annotator1_label`, `annotator2_label`, and
`annotator3_label` in `human_validation_160tweets.csv`.
