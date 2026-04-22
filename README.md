# LLM Agent Memory: A Research Series

A 12-week investigation into how language model agents remember — and why they mostly don't.

## The Question

Long-horizon LLM agents need memory. But "memory" in current systems means one of:
- Stuffing conversation history into context (breaks at scale)
- Summarizing the past (lossy, introduces hallucinations)
- Vector retrieval (retrieves the wrong things under task shift)

**What does a *good* memory system look like — and how would we measure it?**

## Structure

| Week | Notebook                                                                      | Focus                                           |
|------|-------------------------------------------------------------------------------|-------------------------------------------------|
| 1–2  | [01 — Baselines](notebooks/01_baselines.ipynb)                                | Survey + benchmark 3 baseline memory approaches |
| 1–2  | [02 — Summarization Failure Modes](notebooks/02_summarization_failures.ipynb) | Where running summaries lie                     |
| 3–4  | [03 — Hierarchical Memory](notebooks/03_hierarchical_memory.ipynb)            | A 3-tier system from scratch                    |
| 3–4  | [04 — Benchmarking Fairly](notebooks/04_benchmark_comparison.ipynb)           | Controlled head-to-head eval                    |
| 5–6  | [05 — Financial Reasoning](notebooks/05_financial_reasoning.ipynb)            | Where LLMs break on finance tasks               |
| 5–6  | [06 — A Financial Agent That Remembers](notebooks/06_financial_agent.ipynb)   | Memory-augmented BlitZave prototype             |
| 7–8  | [07 — Task-Aware Retrieval](notebooks/07_task_aware_retrieval.ipynb)          | Does context change what you retrieve?          |
| 7–8  | [08 — Decay as a Feature](notebooks/08_decay_as_feature.ipynb)                | Forgetting improves precision                   |
| 9–12 | Paper + distribution                                                          | arxiv synthesis of 3, 4, 7, 8                   |

## Setup

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
cp .env.example .env  # add your API keys
```

## Author

Nemo — ML engineer, building agent memory systems.