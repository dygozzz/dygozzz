## Rodrigo Silva

AI Engineer — LLMs, RAG, semantic search and evaluation. I build the layers underneath:
inference backends, retrieval pipelines, and the harnesses that tell me whether any of it
actually works.

I work in Java, Rust and TypeScript. Currently at Bluedu, where I built the core of two AI
products: a desktop application running local inference (Rust + Tauri, interchangeable
NPU/CPU backends, four-stage hybrid RAG) and a web application with pgvector semantic
search calibrated against a purpose-built benchmark.

**What I care about:** knowing where a number came from. Most of my work is measurement —
including the measurements that failed my own design decisions.

---

### 🔬 [retrieval-pt-br](https://github.com/dygozzz/retrieval-pt-br)

A lab notebook of measured experiments on Portuguese-language retrieval. One question per
experiment, one number per answer.

**Latest finding:** with an English-only tokeniser, Portuguese costs **+54% more tokens**
for the same content — 143 fewer words of usable context in a 512-token window. But there
is no "multilingual tax" (XLM-R costs +1.5%), and a Portuguese-native tokeniser doesn't fix
it either: it just inverts the bill, making English 41% more expensive. The asymmetry
isn't a property of the language — it's a property of what the tokeniser saw during
training.

---

### Stack

**AI/LLM** — RAG · pgvector (HNSW) · embeddings · cross-encoder rerankers · Reciprocal Rank
Fusion · LLM evaluation · prompt engineering · function calling · ONNX Runtime · OpenVINO ·
llama.cpp

**Backend** — Java 21 · Spring Boot · Rust · PostgreSQL (pgvector, Row-Level Security) ·
SQLite · OpenAPI contract-first

**Frontend** — TypeScript · Vue 3 · Nuxt · Angular · Tauri

**Quality** — Playwright · GitHub Actions · benchmarking

---

📍 Bauru, Brazil · 🌐 Portuguese (native), English (C2)

[LinkedIn](https://www.linkedin.com/in/rodrigosilva-736267160) · rodrigo2201silva@gmail.com

Open to AI Engineer and full-stack roles — Brazil, Portugal, Spain.
