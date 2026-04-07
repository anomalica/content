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

High-resource languages (roughly the top 20) produce reliable output from current AI models. Lower-resource languages may produce lower-quality output that is expected to improve as models advance.

Translation corrections can be submitted through the content repository. Corrections are extracted as durable directives that persist across future article regeneration.
