---
title: "Methodology"
description: "How content is produced, from source material to published article."
---

## Pipeline

Content moves through five stages:

1. **Ingestion** - source material (government reports, congressional testimony, court documents, academic papers, news articles, podcast transcripts, recorded interviews) is converted into a standardised record format with metadata about provenance and source type
2. **Digestion** - atomic claims are extracted from records and integrated into a knowledge graph with entities, relationships, and provenance chains
3. **Scoring** - evidence strength is computed algorithmically from attestation level (first-hand, second-hand, third-hand), corroboration across independent sources, and source track record
4. **Assembly** - articles are generated per language from the knowledge graph, with each factual assertion traceable to its source claim
5. **Verification** - an independent AI model from a different provider verifies that assembled content accurately reflects the knowledge graph

## Claims as atomic units

The knowledge graph does not store articles. It stores individual claims - single discrete assertions, each linked to the source document, page, and speaker from which it was extracted. Articles are assembled from these claims, not written as monolithic text. This means the same claim can appear in multiple articles, and every assertion can be independently verified against its source.

## Evidence scoring

Evidence strength is not assigned by editors. It is computed from three factors: how direct the attestation is (did the source witness it, or hear about it from someone who did), how many independent sources corroborate the claim, and the track record of the sources involved. The algorithm is documented in the project's Architecture Decision Records.

## Source material

Anomalica ingests publicly available material only. Each source carries metadata about its type, provenance, and the attestation level of claims within it. The platform does not accept anonymous tips, leaked documents, or material that cannot be attributed to a verifiable source.

## Auditability

Each stage of the pipeline produces a record of its inputs and outputs. Article assembly generates a cryptographic hash of the prompt, knowledge graph state, and output text. This means any article can be independently reproduced from its recorded inputs. A prompt inspector tool allows readers to verify the complete chain from source document to published text.
