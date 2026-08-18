## Rodrigo Silva

Full-Stack Software Engineer working in applied AI — LLMs, RAG, semantic search and
evaluation. I build the layers underneath: inference backends, retrieval pipelines, and
the harnesses that tell me whether any of it actually works.

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

### 📱 [coraGO](https://github.com/dygozzz/coraGO)

An Android travel assistant that runs the LLM **inside the phone** — no server, no API key,
no network call at runtime. Flutter, ~37k lines of Dart.

Qwen 2.5 1.5B via llama.cpp, with **hybrid RAG** before every message (SQLite FTS5/BM25 plus
384-dimension embeddings written in pure Dart) over knowledge packs built from Wikivoyage.

**What I learned building it:** I wrote a full tool-calling layer — eight tools, wired
end to end — and then switched it off. Without a grammar constraining the output, a 1.5B
model emits a tool call for a bare *"hello"*. A false positive on trivial input is worse
than not having the feature, so it stays documented and disabled until a constrained-decoding
runtime is available.

---

### Stack

**AI/LLM** — RAG · pgvector (HNSW) · embeddings · cross-encoder rerankers · Reciprocal Rank
Fusion · LLM evaluation · prompt engineering · function calling · ONNX Runtime · OpenVINO ·
llama.cpp

**Backend** — Java 21 · Spring Boot · Rust · PostgreSQL (pgvector, Row-Level Security) ·
SQLite · OpenAPI contract-first

**Frontend / Mobile** — TypeScript · Vue 3 · Nuxt · Angular · Tauri · Flutter/Dart

**Quality** — Playwright · GitHub Actions · benchmarking

---

📍 Bauru, Brazil · 🌐 Portuguese (native), English (C2)

[LinkedIn](https://www.linkedin.com/in/rodrigo-silva-736267160) · rodrigo2201silva@gmail.com

Open to AI Engineer and full-stack roles — Brazil, Portugal, Spain.
