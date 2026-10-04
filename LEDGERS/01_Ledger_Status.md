# Ledger Status

**Project:** `K_MERLINMEM`  
**Tier:** TIER_4_INFERENCE_AGENTS  
**Identity:** Upstream `mem0ai/mem0` @ `94c3fe9f238f` (Apache-2.0)

## Chain state

| Fact | Value |
| --- | --- |
| Upstream | `mem0ai/mem0` |
| Commit | `94c3fe9f238f3dbf29c9ce98643bd71eb13077cd` |
| Upstream licence | Apache-2.0 |
| Licence class | permissive |
| Clone size | 34.63 MB |
| Ledger | 0 blocks, chain verified |
| Current TRL | NOT YET MEASURED |
| Post-optimisation TRL | NOT YET MEASURED |
| II budget cap | 1000.0 IIU |
| Verified upstream edits | 1 |

- Blocks: **0**
- Head digest: `None`
- Chain verification: **verified**

## Independent verification

The chain is verifiable without trusting this project's tooling:

```
anticloud ledger verify
anticloud ledger export > ledger.jsonl
```

Each block carries the previous block's digest, so removing or reordering an
entry invalidates every block after it. That property is the reason the
ledger can stand in for a claim of what happened.
