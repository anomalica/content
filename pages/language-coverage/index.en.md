---
title: "Language coverage"
description: "Which languages Anomalica supports, how they were chosen, and what coverage they provide."
layout: "language-coverage"
---

Anomalica publishes in 30 languages covering approximately 80% of the world's literate population.

## Selection method

Languages are ranked by incremental coverage using data from the Unicode Common Locale Data Repository, an open dataset maintained by the Unicode Consortium. For each of 244 territories, the dataset provides the percentage of the population that speaks each language, the territory's total population, and its literacy rate.

The selection algorithm is a greedy set-cover: at each step, the language that would cover the most currently-uncovered literate people across all territories is chosen. Overlap between languages within a territory is modelled using an independence assumption. The analysis script, source data, and output are published in the project repository.

## Supported languages

28 translations producing 30 displayed languages. Two additional displayed languages are produced by mechanical conversion: Traditional Chinese (character conversion from Simplified Chinese) and American English (spelling conversion from British English).

## Editorial adjustments

Three languages from the algorithmic top 30 are excluded:

- **Javanese** (rank 21, 32M incremental) - primarily spoken; most literate speakers read Indonesian, supported at position 8
- **Malay** (rank 27, 17M incremental) - mutually intelligible with Indonesian in written form
- **Nigerian Pidgin** (rank 30, 14M incremental) - primarily spoken, not a standard written language for reference works

One language is added:

- **Ukrainian** (rank 33, 13M incremental) - the platform does not support Russian without Ukrainian during an active conflict between the two countries

## Translation quality

High-resource languages (roughly the top 20) produce reliable output from current AI models. Lower-resource languages may produce lower-quality output that is expected to improve as models advance.

Translation corrections can be submitted through the content repository. Corrections are extracted as durable directives that persist across future article regeneration.
