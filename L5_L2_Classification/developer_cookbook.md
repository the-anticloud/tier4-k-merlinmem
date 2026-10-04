# Developer Cookbook — K_MERLINMEM
**Stack:** Python 3.11, SQLite, sentence-transformers, FAISS, PAX 27B, AIOSS_FORMAT
**Domain:** Persistent memory layer for multi-session agent inference: episodic + semantic memory

## Initialize and use memory
```python
from k_merlinmem import MerlinMemory

mem = MerlinMemory(
    db_path="./merlin_memory.db",
    embedding_model="all-MiniLM-L6-v2",
    aioss_chain="./merlin.aioss"
)

# Store episodic memory
mem.store_episode(
    session_id="clinical_agent_001",
    content="Analyzed ECG for patient_hash_abc: detected AF pattern, confidence 0.91",
    timestamp=time.time()
)

# Semantic search over memory
results = mem.search("atrial fibrillation ECG patterns", top_k=5)
for r in results:
    print(f"[{r.score:.2f}] {r.content[:80]}")

# Consolidate session into semantic facts (PAX 27B)
facts = mem.consolidate(session_id="clinical_agent_001",
                        pax_model="./pax-27b-q4.gguf")
print(f"Consolidated {len(facts)} semantic facts")
```

## Forget (GDPR erasure)
```python
mem.forget(session_id="clinical_agent_001")  # deletes episodic + semantic memories
```

## Cross-session context injection
```python
context = mem.get_context_for_session("clinical_agent_002",
                                       query="ECG arrhythmia analysis")
# Returns top-5 relevant memories from past sessions
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```
