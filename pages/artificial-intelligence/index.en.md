---
title: "Artificial intelligence"
description: "How Anomalica uses artificial intelligence, what it does, and what it does not do."
---

## Principle

AI is a tool in the pipeline, not the author. Every factual claim on this platform originates from a human-created source document. AI extracts, arranges, and verifies. It does not generate factual content from its training data.

## Where AI is used

| Stage | What AI does | What AI does not do |
|-------|-------------|-------------------|
| Ingestion | Transcription, text extraction, speaker identification | Generate or infer content |
| Digestion | Identify claims, entities, and relationships | Draw on training data for facts |
| Assembly | Arrange extracted claims into readable articles | Editorially judge claim strength |
| Translation | Produce articles in 30 languages | Alter meaning or add information |
| Verification | Check assembled text against the knowledge graph | Approve or reject content |

## Independent verification

The AI model used for assembly and the model used for verification are from different providers in different jurisdictions. This is a deliberate architectural choice. If one model hallucinates or introduces an error during assembly, the verification model - which has no shared failure modes - is likely to catch it. Geopolitical diversity between providers also reduces the risk of correlated bias.

## Auditability

Each assembly step produces a cryptographic hash of its inputs and outputs. The prompt templates, knowledge graph state, active directives, and generated text are all recorded. This makes the process reproducible: given the same inputs, the same article can be regenerated and compared.

## What this means in practice

If an article states that a specific person said a specific thing at a specific time, that statement traces to a source document where that person is recorded saying it. The AI arranged the claim into readable prose, but the claim itself came from the source. The source document is cited and the relevant passage is identified.

## Transparency commitment

The project publishes its AI constraints, assembly architecture, and verification process as Architecture Decision Records. These are open to public review and challenge. See [Decisions](/decisions/) for the full record.
