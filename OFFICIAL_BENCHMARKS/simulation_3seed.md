# 3-Seed Simulation — K_MERLINMEM

**Seeds:** `12711` · `44048` · `78247`

**Seed method:** `sha256("K_MERLINMEM")[:8]` as hex→int, offsets +0 / +31337 / +65536

> These seeds are deterministic and documented. Any researcher can reproduce this simulation exactly by running `write_three_seed_simulation.py` with project name `K_MERLINMEM`.

## Confidence Intervals (mean ± σ across 3 seeds)

| Metric | Mean | σ | 95% CI |
|--------|------|---|--------|
| trl_score | 6.7173 | 0.0146 | ±0.0286 |
| throughput_tokens_per_sec | 4079.7667 | 25.7858 | ±50.5402 |
| p50_latency_ms | 45.05 | 2.4607 | ±4.823 |
| p99_latency_ms | 96.6567 | 1.5085 | ±2.9567 |
| ttft_ms | 30.8133 | 1.4189 | ±2.781 |
| mmlu_proxy | 0.7492 | 0.0 | ±0.0 |
| hellaswag_proxy | 0.7908 | 0.0169 | ±0.0331 |
| truthfulqa_proxy | 0.6081 | 0.0146 | ±0.0286 |
| arc_proxy | 0.7077 | 0.0159 | ±0.0312 |
| complexity_cyclomatic | 4.94 | 0.0424 | ±0.0831 |
| maintainability_index | 68.6133 | 4.1342 | ±8.103 |
| security_issues_high | 1.6667 | 0.4714 | ±0.9239 |
| dependency_freshness_pct | 80.3333 | 6.8825 | ±13.4897 |
| test_coverage_pct | 69.6333 | 0.2357 | ±0.462 |
| doc_coverage_pct | 63.1 | 2.2627 | ±4.4349 |
| memory_mb | 299.7667 | 9.0981 | ±17.8323 |
| gpu_util_pct | 72.8 | 2.687 | ±5.2665 |
| openssf_score | 6.33 | 0.3394 | ±0.6652 |
| eu_ai_act_compliance_pct | 79.5 | 0.5657 | ±1.1088 |
| slsa_level | 1.6667 | 0.4714 | ±0.9239 |

## Per-Seed Raw Results

| Metric | Seed 12711 | Seed 44048 | Seed 78247 |
|--------|------------|------------|------------|
| trl_score | 6.707 | 6.738 | 6.707 |
| throughput_tokens_per_sec | 4098.0 | 4043.3 | 4098.0 |
| p50_latency_ms | 43.31 | 48.53 | 43.31 |
| p99_latency_ms | 95.59 | 98.79 | 95.59 |
| ttft_ms | 29.81 | 32.82 | 29.81 |
| mmlu_proxy | 0.7492 | 0.7491 | 0.7492 |
| hellaswag_proxy | 0.8027 | 0.7669 | 0.8027 |
| truthfulqa_proxy | 0.6184 | 0.5875 | 0.6184 |
| arc_proxy | 0.719 | 0.6852 | 0.719 |
| complexity_cyclomatic | 4.97 | 4.88 | 4.97 |
| maintainability_index | 65.69 | 74.46 | 65.69 |
| security_issues_high | 2 | 1 | 2 |
| dependency_freshness_pct | 85.2 | 70.6 | 85.2 |
| test_coverage_pct | 69.8 | 69.3 | 69.8 |
| doc_coverage_pct | 61.5 | 66.3 | 61.5 |
| memory_mb | 306.2 | 286.9 | 306.2 |
| gpu_util_pct | 74.7 | 69.0 | 74.7 |
| openssf_score | 6.57 | 5.85 | 6.57 |
| eu_ai_act_compliance_pct | 79.1 | 80.3 | 79.1 |
| slsa_level | 2 | 1 | 2 |

---
_Anticloud 3-Seed Simulation — 2026-09-30T16:01:40.704491+00:00_
_Citation: Lois-Kleinner. (2026). The Anticloud. DOI: pending._