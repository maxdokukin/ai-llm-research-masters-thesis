# Knowledge-Graph Context Assembly — Master's thesis on context engineering for LLMs

CMPE 299A — Master's Thesis (MS Computer Engineering), San José State University · Fall 2026 – ongoing · Solo, advisor Mahima Agumbe Suresh · In progress

## Overview

Large language models are a core component of modern human-computer interaction, and their answer quality and
computational cost depend strongly on the information placed in the input context. This thesis studies *context
assembly*: choosing which information enters the model's input, under a token budget, so that answers improve while
the model reads less. It proposes a knowledge-graph-based representation of context and an assembly function for
context selection and multi-agent collaboration. The work is at the proposal and prototype stage; the detailed design
is not published while the research is in progress.

## Highlights

- Thesis topic and abstract defined; research direction narrowed from three candidate paths to one (Fall 2026).
- Early end-to-end prototype of graph-based context assembly, built on a temporal knowledge-graph framework, with a
  small web demo that shows what was selected for each question — runs offline with an automated test suite.
- Research vault with 15 reviewed papers and an agent-assisted literature workflow (search, pull, summarise,
  highlight → evidence-backed concept graph).

## How it works

```
papers → vault notes → context units in a knowledge graph
      → query-conditioned budgeted selection → LLM answer + inspectable selection trace
```

- **Research vault** — Obsidian vault driven by a Claude Code skill and small Python scripts; papers come in with a
  summary and a relevance note, highlights become concept notes and evidence.
- **Context-assembly prototype** — Python package (Graphiti on FalkorDB Lite, FastAPI demo, Jupyter notebooks,
  pytest) that stores context units in a knowledge graph and assembles a budgeted context per query. Model calls are
  recorded once and replayed, so everything runs without API access.

## Getting started

```bash
# prototype (private repo)
git clone https://github.com/maxdokukin/context-assembly-sample-graph.git && cd context-assembly-sample-graph
./run.sh              # local demo in replay mode; see README for notebooks and tests

# research vault (private repo)
git clone https://github.com/maxdokukin/research.git && cd research
./setup.sh && cd vault && claude
```

## Documents

- `docs/thesis_abstract.pdf` — thesis abstract (Fall 2026)
- Research-topics deck and advisor meeting notes — internal, not published
