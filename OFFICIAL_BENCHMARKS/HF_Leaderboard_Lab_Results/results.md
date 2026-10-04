# HF_Leaderboard_Lab_Results

**Project:** `K_MERLINMEM`  
**Tier:** `TIER_4_INFERENCE_AGENTS`  
**Slug:** `mem0ai/mem0`  
**Commit:** `94c3fe9f238f`  
**Run:** `2026-09-30T15:07:07.146295+00:00`  

## Isolation Environment

| Field | Value |
| ----- | ----- |
| Platform | `win32` |
| Python | `3.12.10` |
| HF model | `distilbert-base-uncased` |
| HF load time | `4.42s` |
| Inference device | `cpu` |

## Results

**Framework:** [HuggingFace Open LLM Leaderboard (proxy via distilbert-base-uncased)](https://huggingface.co/docs/leaderboards/en/open_llm_leaderboard/archive)

**Model used:** `distilbert-base-uncased`

### Inference Latency (Classification)

| Metric | Value |
| ------ | ----- |
| Avg latency | **49.01 ms** |
| Min latency | 43.53 ms |
| Max latency | 56.0 ms |
| Samples | 5 |

### Real Tokenization Results

| Field | Value |
| ----- | ----- |
| Token count | **42** |
| Tokenization latency | 1.0 ms |
| Classification label | `LABEL_0` |
| Classification score | 0.5847 |
| Classification latency | 103.54 ms |
| Status | **PASS** |

**Input text tokenized:**
```
K_MERLINMEM (mem0ai/mem0) — 1836 files, 237714 source lines, licence Apache-2.0, primary language ['TypeScript']
```

**First 20 tokens:**
```
['[CLS]', 'k', '_', 'merlin', '##me', '##m', '(', 'me', '##m', '##0', '##ai', '/', 'me', '##m', '##0', ')', '—', '1836', 'files', ',']
```

> Full MMLU/HellaSwag/TruthfulQA/ARC/Winogrande/GSM8K require dedicated GPU.
> These results are CPU inference proxy metrics using distilbert-base-uncased.

---
_Anticloud Benchmark Suite — isolation log — 2026-09-30T15:07:07.146295+00:00_