# Wave Field LLM

A novel attention mechanism for language models that achieves **O(N log N)** complexity, replacing the standard O(N²) dot-product attention.

Tokens interact through wave propagation on a continuous field rather than direct pairwise comparison — enabling efficient scaling to long contexts that are impossible with standard transformers.

## Key Results

| Metric | Value |
|---|---|
| DCLM CORE (130M model) | **46.8%** (GPT-2 target: 26.5%) |
| Throughput at 32K context | **21.8x faster** than standard |
| Memory at 32K context | **5.3x less** than standard |
| 128K context | **Runs** (standard OOMs) |

See [BENCHMARKS.md](BENCHMARKS.md) for full results.

## Status

Active research. Scaling to larger models. Patent pending.

---

*Built by Badaramoni Avinash*
