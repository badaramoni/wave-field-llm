# Wave Field LLM — Benchmarks

## DCLM CORE (Zero-shot, 1000 samples)

| Task | Wave Field 130M | GPT-2 Small (124M) |
|---|---|---|
| ARC Easy | **43.8%** | 25.0% |
| HellaSwag | **31.8%** | 25.0% |
| PIQA | **61.7%** | 50.0% |
| WinoGrande | **49.8%** | 50.0% |
| **Average** | **46.8%** | **26.5%** |

## DCLM Extended (Zero-shot)

| Task | Score |
|---|---|
| PIQA | 61.7% |
| SciQ | 57.2% |
| Copa | 54.0% |
| BoolQ | 50.6% |
| WinoGrande | 49.8% |
| ARC Easy | 43.8% |
| HellaSwag | 31.8% |
| ARC Challenge | 18.7% |
| OpenBookQA | 16.4% |
| Lambada | 1.1% |
| **Average (10 tasks)** | **38.5%** |

## Throughput (H100 SXM, matched params)

| Context | Standard O(N²) | Wave Field O(N log N) | Speedup |
|---|---|---|---|
| 2K | 716K tok/s | 724K tok/s | 1.0x |
| 8K | 361K tok/s | 1,629K tok/s | **4.5x** |
| 32K | 101K tok/s | 2,216K tok/s | **21.8x** |
| 128K | OOM | 1,583K tok/s | **∞** |

## Memory

| Context | Standard | Wave Field | Reduction |
|---|---|---|---|
| 32K | 35.6 GB | 6.74 GB | **5.3x** |
| 128K | OOM | 26.76 GB | **Standard cannot run** |

## Training

| | 130M model | 1.49B model |
|---|---|---|
| Tokens | 32B | 6.8B |
| Hardware | 2× RTX 5090 | 8× H100 SXM |
| Time | 54.4 hours | 11.5 hours |
| Checkpoint | 505 MB | 5.7 GB |
| DCLM CORE | 46.8% | 39.8% |

---

*Built by Badaramoni Avinash*
