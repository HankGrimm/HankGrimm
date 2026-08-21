<div align="center">

# Hank Grimm

**Agent / AI Engineering · CS @ Guangzhou College of Commerce · Guangzhou**

Building AI-native full-stack systems — from Multi-Agent workflows to security-hardened backend migrations.

[![GitHub](https://img.shields.io/badge/GitHub-HankGrimm-181717?style=flat&logo=github)](https://github.com/HankGrimm)
[![Email](https://img.shields.io/badge/Email-hankgrimm91%40gmail.com-EA4335?style=flat&logo=gmail)](mailto:hankgrimm91@gmail.com)
[![Visitors](https://komarev.com/ghpvc/?username=HankGrimm&color=brightgreen&style=flat&label=Profile+Views)](https://github.com/HankGrimm)

</div>

---

### 💼 Experience

**AI Full-Stack Intern · Baidu (China) Co., Ltd. Guangzhou Branch** `2026.07 – 2026.08`

Led the security-hardening rewrite of the `e.baidu` backend system.

- Designed and led a strangler-fig migration from a `ThinkCMF 6 + ThinkPHP 6` PHP monolith to `NestJS 10 + TypeScript`, fixing P0 vulnerabilities (arbitrary SQL execution via WebSocket, hardcoded credentials, superuser hard-bypass)
- Implemented zero-trust JWT gateway integration (UUAP), dual-guard RBAC with strict-deny defaults, and hashed sensitive-field indexing
- Migrated **30 read-only API paths / 39 operations** with **85 Jest tests** passing; shipped a React 18 + Ant Design Pro admin frontend with an SSE-streamed agent chat preview (**13 Vitest tests** passing)

**AI/LLM Engineering Intern · Guangzhou Xin'an Data Co., Ltd.** `2026.04 – 2026.07`

Built Multi-Agent document review pipelines for enterprise brand & KPI compliance systems.

- Orchestrated multi-node Agent workflows with `Dify`, converting manual report review into a fully automated pipeline across 7 intent-routed review dimensions
- Optimized RAG retrieval (hierarchical Markdown chunking + Hybrid Search + Reranker on `Milvus`) — QA accuracy **60% → 88%**
- Built a provider-agnostic LLM connection pool with exponential backoff, token-bucket rate limiting, and streaming support

**Founder / Full-Stack Developer · Guangzhou BoBaCarry Smart Tech Co., Ltd.** `2025.09 – 2026.04`

Built a shared smart-follow-cart platform end-to-end, from WeChat Mini Program to production deployment.

- `Node.js + Express` backend with `MySQL + Redis` (**<50ms** response latency); `Vue 3 + Element Plus` ops console
- Defined MQTT device protocol with hardware engineers; built a device simulator to unblock firmware integration before hardware arrived

---

### 🌱 Open Source Contributions

Contributing to the **Vercel AI SDK** ecosystem (`vercel/ai`, `vercel/ai-elements`) — CSS layout fixes, TypeScript API design, and batch-processing algorithm design for the core `embedMany` function.

| Repo | Type | Status |
|---|---|---|
| [vercel/ai-elements #476](https://github.com/vercel/ai-elements/pull/476) | Fix: `overflow-hidden` → `overflow-x-clip` (sticky positioning) | In review |
| [vercel/ai-elements #477](https://github.com/vercel/ai-elements/pull/477) | Fix: decouple `ImageProps` from deprecated SDK type | In review |
| [vercel/ai-elements #478](https://github.com/vercel/ai-elements/pull/478) | Fix: Enter-key guard bypass during streaming | In review |
| [vercel/ai #10082](https://github.com/vercel/ai/issues/10082) | Proposal: token-aware batching for `embedMany` | Awaiting maintainer feedback |

---

### 📌 Projects

**[HUM / Voices](https://github.com/HankGrimm)** — Emotional voice-persona platform `2026.01 – 2026.02`

> Winner, AI³ Growth Journey Season 8. Each Voice = timbre (StepFun API cloning) + personality + emotional-boundary strategy.

- SSE-streamed TTS with React state + Audio Context double-buffering — **<300ms** time-to-first-audio
- Redis semantic/audio caching cut repeated-dialogue TTS cost by **45%**
- On-chain persona provenance on `0G` (AI + Data native chain)

`TypeScript` `React` `Node.js` `PostgreSQL` `Redis` `Docker` `StepFun API`

**EdTech Platform** — Adaptive learning path generation `2025.11 – 2026.01`

- Extended `BKT` cognitive diagnosis model with Redis-backed real-time mastery-probability updates
- Few-shot-injected BKT mastery state into `Gemini API` for difficulty-calibrated question generation

`Spring Boot` `Gemini API` `React` `RabbitMQ` `MyBatis Plus`

**indicator_detector** — KPI quality detection & recommendation `2026.04 – 2026.05`

- Hybrid scalar-filter + vector-similarity retrieval on `Milvus Lite` for multi-tenant Top-K KPI recommendation
- ReAct-style prompt design (Few-shot + CoT) for formula-dependency parsing with self-correcting JSON Schema output

`Python` `Milvus Lite` `Transformers` `PyTorch`

---

### 🧰 Tech Stack

<div align="center">

[![Skills](https://skillicons.dev/icons?i=python,ts,java,go,solidity,react,vue,nextjs,tailwind,nestjs,spring,nodejs,mysql,postgres,redis,docker,nginx,linux,git)](https://skillicons.dev)

</div>

`Multi-Agent Orchestration (Dify)` `RAG (Hybrid Search + Rerank)` `Prompt Engineering (CoT/Few-shot)` `LLM Connection Pooling` `JWT/RBAC` `Zero-Trust Gateway`

---

<div align="center">

154+ contributions this year · 23 public repos · Pull Shark 🦈

</div>
