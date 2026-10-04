# L5 Narrow / L2 General Classification — K_MERLINMEM
**Platform:** Anticloud | **Tier:** TIER_4_INFERENCE_AGENTS | **PAX:** 27B
**IP:** USPTO pending 2026, Anticloud FZ LLE, 0-1.gg | **License:** Apache-2.0

## L5 Narrow
K_MERLINMEM provides persistent episodic and semantic memory for Anticloud inference agents. Narrow scope: Anticloud agent sessions only. Episodic memory stores past interaction summaries; semantic memory indexes key facts derived from interactions. Both are locally encrypted and AIOSS-chained.

## L2 General
L2 General: any TIER_4 agent that needs cross-session context uses K_MERLINMEM. Clinical agents remember past patient encounter patterns; robotics agents remember past mission failures — same memory API for both.

## PAX 27B Integration
PAX 27B performs memory consolidation: after a session, PAX summarizes episodic memories into semantic facts that are inserted into KANTOR_K5 and indexed in KAMELOT_SEARCH for future retrieval.

## AIOSS Audit Chain
Every memory operation (session hash + memory type + content hash + retrieval score when queried) is chained: H_n = SHA3-256(H_{n-1} || entry_hash_n || timestamp_n).
Offline-verifiable, tamper-evident, zero cloud dependency.

## Regulatory / Compliance
GDPR Art. 17 (right to erasure for stored memories). ISO 27001 A.8.2 (information classification).
