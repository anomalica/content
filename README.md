# anomalica-content

Assembled content for the Anomalica encyclopaedia. This repository is the output of the assembly pipeline and the input to the static site.

Content is organised document-first: each document is a directory containing all its language versions, review data, and verification reports. See the [content lifecycle architecture](https://github.com/anomalica/anomalica/blob/main/architecture/content-lifecycle.md) for the full structure.

The assembler writes markdown body content but never modifies frontmatter. Directives (instructions to the assembler) live in each document's frontmatter. Human reviews live in sidecar `review.yaml` files.

Static pages (legal documents, policy pages) are maintained by hand rather than assembled from the knowledge graph, but follow the same directory structure and review system.
