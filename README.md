# Wave Field LLM

A novel attention mechanism for language models that achieves **O(N log N)** complexity, replacing the standard O(N²) dot-product attention.

## Key Results

| Metric | Value |
|---|---|
| DCLM CORE (130M model) | **46.8%** (GPT-2 target: 26.5%) |
| Throughput at 32K context | **21.8x faster** than standard |
| Memory at 32K context | **5.3x less** than standard |
| 128K context | **Runs** (standard OOMs) |
| Inference | **O(1) per token** — constant speed at any context length |
| Compression | **3.1x** via INT8, quality preserved |

See [BENCHMARKS.md](BENCHMARKS.md) for full results.

## What We've Achieved

- Trained models from 130M to 1.5B parameters
- O(N log N) training complexity via FFT convolution
- **O(1) inference** — constant memory, constant speed regardless of context length
- Runs on consumer GPUs — no data center required
- 80+ tokens/sec on a laptop
- Architecture currently at **v9** — actively scaling

## Why It Matters

Standard transformers slow down and run out of memory as context grows. Wave Field doesn't. The architecture maintains constant inference cost whether the context is 1K or 1M tokens.

## Links

- **Website:** [wavefieldlab.com](https://wavefieldlab.com)
- **LinkedIn:** [Avinash Badaramoni](https://www.linkedin.com/in/avinashbadaramoni/)

## Status

Active research. Scaling to larger models. Patent pending.

---

*Built by Badaramoni Avinash*
