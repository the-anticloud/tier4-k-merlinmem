# Deploy Guide — K_MERLINMEM
**Tier:** TIER_4_INFERENCE_AGENTS | **Stack:** Python 3.11, SQLite, sentence-transformers, FAISS, PAX 27B, AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, SQLite (stdlib), sentence-transformers, FAISS-cpu 1.7+, PAX 27B.

## Environment
4GB RAM for memory index. CPU-only for memory read/write. GPU for PAX consolidation pass.

## AIOSS Integration
```bash
aioss init --module K_MERLINMEM --output ./k_merlinmem.aioss
aioss append --chain ./k_merlinmem.aioss --payload ./output.bin --module K_MERLINMEM
aioss verify --chain ./k_merlinmem.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="K_MERLINMEM",
    aioss_chain="./K_MERLINMEM.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./K_MERLINMEM.aioss --verbose
python -m K_MERLINMEM.tests.smoke
```
