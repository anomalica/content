---
title: "Language coverage"
description: "Which languages Anomalica supports, how they were chosen, and what coverage they provide."
layout: "language-coverage"
---

Anomalica publishes in 30 languages covering approximately 80% of the world's literate population. Languages are selected algorithmically by incremental coverage of literate people, using open data from the Unicode Common Locale Data Repository.

At each step, the language covering the most currently-uncovered literate people is chosen. The selection script, source data, and output are published in the project repository.

<!-- split -->

## Editorial adjustments

Three languages from the algorithmic top 30 are excluded:

- **Javanese** (rank 21, 32M) - primarily spoken; most literate speakers read Indonesian, supported at position 8
- **Malay** (rank 27, 17M) - mutually intelligible with Indonesian in written form
- **Nigerian Pidgin** (rank 30, 14M) - primarily spoken, not a standard written language for reference works

One language is added:

- **Ukrainian** (rank 33, 13M) - the platform does not support Russian without Ukrainian during an active conflict between the two countries

28 translations produce 30 displayed languages. Traditional Chinese is a mechanical character conversion from Simplified Chinese, and American English is a spelling conversion from British English.

## Translation quality

AI translation quality varies measurably by language. The WMT24 shared task (the standard academic benchmark for machine translation) found that large language models now outperform conventional translation systems across all 55 languages tested, but with a clear quality gradient.

WMT24 CometKiwi scores for English-to-target translation (higher is better, scale 0 to 1):

| Language pair | Best LLM score | Quality |
|---|---|---|
| English to Japanese | 0.762 | Strong |
| English to Spanish | 0.745 | Strong |
| English to Russian | 0.742 | Strong |
| English to Ukrainian | 0.732 | Strong |
| English to German | 0.723 | Strong |
| English to Chinese | 0.726 | Strong |
| English to Hindi | 0.657 | Moderate |

Hindi, the highest-resourced language in the Indic family, scores 0.06 to 0.10 lower than European and CJK languages. Languages with less training data (Burmese, Uzbek, Marathi) can be expected to show a larger gap, though published benchmark data for these specific languages is limited.

Based on available benchmarks, the 28 translated languages fall into three tiers:

- **Strong** (11 languages): French, German, Spanish, Portuguese, Russian, Chinese, Japanese, Italian, Polish, Korean, Ukrainian
- **Moderate** (14 languages): Arabic, Hindi, Turkish, Vietnamese, Indonesian, Thai, Bengali, Urdu, Persian, Swahili, Tamil, Telugu, Tagalog, Marathi
- **Limited data** (3 languages): Burmese, Uzbek, Tamil

For the third tier, published translation benchmarks are sparse. Meta's NLLB-200 model scores Burmese lowest of all 28 languages on the FLORES benchmark (chrF++ 30.9 vs French at 69.6), though larger models perform substantially better than NLLB.

Translation corrections can be submitted through the content repository. Corrections are extracted as durable directives that persist across future article regeneration.

Sources: [WMT24 General MT Ranking](https://arxiv.org/abs/2407.19884), [WMT24++ 55-language expansion](https://arxiv.org/abs/2502.12404), [NLLB-200 FLORES metrics](https://dl.fbaipublicfiles.com/nllb/nllb200_3b_metrics.csv).
