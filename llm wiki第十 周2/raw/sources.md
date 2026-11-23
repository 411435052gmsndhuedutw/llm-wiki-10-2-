# Source Ingestion Register

This Wiki ingests five sources for the design of an evidence-grounded, interactive study assistant. The sources support the workflow and system design; the sample quiz is explicitly marked as a walkthrough, not a live generated result.

## S1 — Building Effective Agents

- **Author:** Anthropic
- **Type:** Engineering article
- **URL:** https://www.anthropic.com/research/building-effective-agents
- **Ingested points:** Distinguishes fixed workflows from agents that dynamically direct their process; describes evaluator-optimizer loops, tool feedback, human checkpoints, and iteration limits.
- **Used in:** [Agentic workflow patterns](../wiki/article1.md), [workflow design](../wiki/workflow.md)
- **Caveat:** The article notes that its tooling landscape has changed since its original publication. This Wiki uses its general patterns, not its framework recommendations.

## S2 — ReAct: Synergizing Reasoning and Acting in Language Models

- **Authors:** Shunyu Yao et al.
- **Type:** Research paper, arXiv:2210.03629, v3 (ICLR camera-ready)
- **URL:** https://arxiv.org/abs/2210.03629
- **Ingested points:** Interleaves reasoning traces and task actions; observations from external sources can inform later decisions.
- **Used in:** [Question-level loop](../wiki/article2.md), [exam-notes example](../wiki/study-notes.md), [evidence-card walkthrough](../wiki/evidence-cards.md)
- **Limit:** ReAct is a design pattern, not a guarantee that every generated answer is correct.

## S3 — Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks

- **Authors:** Patrick Lewis et al.
- **Type:** Research paper, arXiv:2005.11401, NeurIPS 2020
- **URL:** https://arxiv.org/abs/2005.11401
- **Ingested points:** Combines a language model with retrieved non-parametric knowledge; provenance and updating knowledge remain important challenges.
- **Used in:** [Grounding answers in course materials](../wiki/article3.md), [evidence cards](../wiki/evidence-cards.md)
- **Limit:** Retrieval can provide relevant passages but does not by itself prove that a generated answer follows from them.

## S4 — LangGraph Graph API Overview

- **Author:** LangChain documentation
- **Type:** Official technical documentation
- **URL:** https://docs.langchain.com/oss/python/langgraph/graph-api
- **Ingested points:** Models a graph using shared state, nodes, and edges; edges can be fixed or conditional, and graphs can include sequences, branches, and loops.
- **Used in:** [Graph structure](../wiki/article4.md), [workflow specification](../wiki/workflow.md)

## S5 — Evaluate Agent Workflows

- **Author:** OpenAI documentation
- **Type:** Official technical documentation
- **URL:** https://developers.openai.com/api/docs/guides/agent-evals
- **Ingested points:** Uses traces to inspect end-to-end agent behavior and repeatable datasets/evaluation runs to compare workflow changes.
- **Used in:** [Verification and evaluation](../wiki/article5.md), [execution record](../wiki/log.md)

## Ingestion method

Each source was read and reduced to a short source card: claim, relevant workflow implication, limitation, and planned Wiki use. The slide deck cites the Wiki pages; the Wiki pages retain direct source links.
