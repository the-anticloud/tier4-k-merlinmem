# Radon_Complexity_Lab_Results
**Project:** `K_MERLINMEM` | **Status:** `PASS` | **Run:** `2026-09-30T17:14:20.030944+00:00`

**Framework:** [Radon — Cyclomatic Complexity & Maintainability Index](https://radon.readthedocs.io/)

## Key Metrics

- **files_analyzed:** `10`
- **average_complexity:** `{'grade': 'A', 'score': 2.642857142857143}`
- **complexity_grade:** `A`
- **complexity_score:** `2.642857142857143`
- **mi_output:** `E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_MERLINMEM\UPSTREAM\mem0\exceptions.py - A (44.16)
E:\fenta\Do`

## Raw Output (first 50 lines)
```
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_MERLINMEM\UPSTREAM\mem0\exceptions.py
    F 424:0 create_exception_from_response - A (5)
    C 34:0 MemoryError - A (3)
    M 58:4 MemoryError.__init__ - A (3)
    C 304:0 VectorStoreError - A (2)
    C 326:0 EmbeddingError - A (2)
    C 346:0 LLMError - A (2)
    C 366:0 DatabaseError - A (2)
    C 386:0 DependencyError - A (2)
    M 82:4 MemoryError.__repr__ - A (1)
    C 93:0 AuthenticationError - A (1)
    C 115:0 RateLimitError - A (1)
    C 138:0 ValidationError - A (1)
    C 162:0 MemoryNotFoundError - A (1)
    C 179:0 NetworkError - A (1)
    C 202:0 ConfigurationError - A (1)
    C 224:0 MemoryQuotaExceededError - A (1)
    C 246:0 MemoryCorruptionError - A (1)
    C 263:0 VectorSearchError - A (1)
    C 286:0 CacheError - A (1)
    M 318:4 VectorStoreError.__init__ - A (1)
    M 340:4 EmbeddingError.__init__ - A (1)
    M 360:4 LLMError.__init__ - A (1)
    M 380:4 DatabaseError.__init__ - A (1)
    M 400:4 DependencyError.__init__ - A (1)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_MERLINMEM\UPSTREAM\mem0\_anticloud_egress.py
    F 38:0 _is_frontier - A (4)
    F 43:0 guarded_connect - A (4)
    F 61:0 install - A (3)
    F 33:0 is_offline - A (1)
    C 29:0 EgressDenied - A (1)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_MERLINMEM\UPSTREAM\scripts\check-llms-txt-coverage.py
    F 93:0 main - B (10)
    F 41:0 load_ignore_prefixes - A (5)
    F 52:0 canonical_repo_pages - A (4
```

---
_Anticloud Independent Benchmark — 2026-09-30T17:14:20.030944+00:00_