<div align="center">

# Hank Grimm · 韩广宁

**Agent / AI Engineering · CS @ Guangzhou College of Commerce · Guangzhou**

Building AI-native full-stack systems — from Multi-Agent workflows to security-hardened backend migrations.

<img src="assets/logos/baidu.svg" alt="Baidu" width="115" /> &nbsp;&nbsp;&nbsp;
<img src="assets/logos/anker.svg" alt="Anker Innovations" width="115" /> &nbsp;&nbsp;&nbsp;
<img src="assets/logos/feishu.svg" alt="Feishu" width="105" />

[![GitHub](https://img.shields.io/badge/GitHub-HankGrimm-181717?style=flat&logo=github)](https://github.com/HankGrimm)
[![Email](https://img.shields.io/badge/Email-hankgrimm91%40gmail.com-EA4335?style=flat&logo=gmail)](mailto:hankgrimm91@gmail.com)
[![Visitors](https://komarev.com/ghpvc/?username=HankGrimm&color=brightgreen&style=flat&label=Profile+Views)](https://github.com/HankGrimm)

</div>

---

### 🏆 Honors & Awards

- **Champion, Security Track — Anker Innovations 1st Hackathon Challenge (安克创新首届黑客松挑战赛 · 安防赛道冠军)** `2026`
- **Champion, AI³ Growth Journey Season 8** `2026`
- **Champion, ConsensusHK** `2026`
- **National Top 40, 2026 AI Pioneer Future Talent Competition (2026 AI 先锋未来人才大赛)** `2026`
- **National First Prize, National College Students' "Innovation, Creativity & Entrepreneurship" E-Commerce Challenge (全国大学生电子商务「创新、创意及创业」挑战赛)** `2026`

---

### 💼 Experience

**AI Full-Stack Intern · Baidu (China) Co., Ltd. Guangzhou Branch** `2026.07 – 2026.10`

Security-hardening rewrite of the `e.baidu` backend, plus marketing landing pages and conversion data pipelines.

- Designed and drove a strangler-fig migration from a PHP monolith to `NestJS 10 + TypeScript`, resolving multiple P0 auth-bypass and identity-spoofing issues along the way
- Integrated SSO via a unified identity gateway with dual-guard JWT auth (401 unbound / 403 no-role), RBAC consolidation, and hashed sensitive-field indexing
- Migrated **30 read-only API paths / 39 operations** with **85 Jest tests** passing; shipped a React 18 + Ant Design Pro admin frontend with an SSE-streamed agent chat preview (**13 Vitest tests** passing)
- Shipped **40+** multi-channel landing pages; built a `create-lp-from-images` Skill that generates and publishes a landing page from design slices + a prompt

**AI/LLM Engineering Intern · Guangzhou Xin'an Data Co., Ltd.** `2026.04 – 2026.07`

Built Multi-Agent document review pipelines for enterprise brand & KPI compliance systems.

- Orchestrated multi-node Agent workflows with `Dify`, converting manual report review into a fully automated pipeline across 7 intent-routed review dimensions
- Optimized RAG retrieval (hierarchical Markdown chunking + Hybrid Search + Reranker on `Milvus`) — QA accuracy **60% → 88%**
- Built a provider-agnostic LLM connection pool with exponential backoff, token-bucket rate limiting, and streaming support

**Founder / Full-Stack Developer · Guangzhou Kangxiaomiao Smart Technology Co., Ltd. (BoBaCarry)** `2025.09 – 2026.04`

Built a shared smart-follow-cart platform end-to-end, from WeChat Mini Program to production deployment.

- `Node.js + Express` backend with `MySQL + Redis` (**<50ms** response latency); `Vue 3 + Element Plus` ops console
- Defined MQTT device protocol with hardware engineers; built a device simulator to unblock firmware integration before hardware arrived

---

### 🌱 Open Source Contributions

Contributing across the AI/agent ecosystem — from MCP servers and the Vercel AI SDK's frontend components to Python event-bus internals and cross-platform CI correctness.

| Repo | Type | Status |
|---|---|---|
| [line/line-bot-mcp-server #590](https://github.com/line/line-bot-mcp-server/pull/590) | Feat: add `get_group_summary` MCP tool | ✅ Merged |
| [NandhaKishorM/laya #216](https://github.com/NandhaKishorM/laya/pull/216) | Fix: cross-platform encoding/CRLF bug in CI benchmark audit | ✅ Merged |
| [browser-use/bubus #35](https://github.com/browser-use/bubus/pull/35) | Feat: `EventBus.remove()` to unsubscribe handlers | In review |
| [browser-use/jev-ultrafast #188](https://github.com/browser-use/jev-ultrafast/pull/188) | Fix: browser-agent process leak after recording | In review |
| [HKUDS/nanobot #5729](https://github.com/HKUDS/nanobot/pull/5729) | Fix: deterministic hash for WeCom/WeChat media fallback names | In review |
| [vercel/ai-elements #476](https://github.com/vercel/ai-elements/pull/476) | Fix: `overflow-hidden` → `overflow-x-clip` (sticky positioning) | In review |
| [vercel/ai-elements #477](https://github.com/vercel/ai-elements/pull/477) | Fix: decouple `ImageProps` from deprecated SDK type | In review |
| [vercel/ai-elements #478](https://github.com/vercel/ai-elements/pull/478) | Fix: Enter-key guard bypass during streaming | In review |
| [gokite-ai/kite-x402-services #2](https://github.com/gokite-ai/kite-x402-services/pull/2) | Feat: add Frankfurter FX x402 service | In review |
| [vercel/ai #10082](https://github.com/vercel/ai/issues/10082) | Discussion: proposed token-aware batching for `embedMany` | Closed |

---

### 📌 Projects

**[ParTrace Vision 驿站追迹](https://github.com/SUertee/partrace-vision)** — AI event-tracing agent for parcel stations `2026.10`

> 🏆 Champion, Security Track — Anker Innovations 1st Hackathon. Android (Kotlin + Compose) + FastAPI + Agent package + Vision worker, PostgreSQL + pgvector, deployed on AWS.

- Anti-hallucination delivery: agent replies ship with deterministic cards assembled only from verified tool payloads; SSE run-event stream with snapshot-first + `Last-Event-ID` resume
- Passwordless Aurora IAM auth: stdlib SigV4 presigning byte-identical to `aws rds generate-db-auth-token`, IMDSv2 role credentials, zero new dependencies
- Spec-driven development with OpenSpec: 11 tables / 27 APIs aligned across modules, SQL, and OpenAPI, guarded by a docs-consistency CI

`Python` `FastAPI` `PostgreSQL` `pgvector` `AWS` `Kotlin`

**[LingMate 聆伴](https://github.com/strawberry77-1/LingMate)** — AI voice life assistant for the elderly (Age Well Hackathon) `2026.08`

- `LangGraph` StateGraph (`understand → execute → respond`) routing to 5 single-purpose sub-agents with slot filling and natural-language time parsing
- Three-layer anti-fraud detection: weighted rule engine + RAG similar-case retrieval + LLM review; rules keep working when the model is down (**34/34** unit tests)
- Voice pipeline: Vosk offline ASR + Tencent Cloud ASR/TTS with graceful fallbacks; OpenAI-compatible LLM layer over Hunyuan / DeepSeek

`Python` `LangGraph` `FastAPI` `React 19`

**[HUM / Voices 人声余温](https://github.com/Chengyuann/HUM)** — Emotional voice-persona platform `2026.01 – 2026.02`

> 🏆 Winner, AI³ Growth Journey Season 8. Each Voice = timbre (StepFun API cloning) + personality + emotional-boundary strategy.

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

[![Skills](https://skillicons.dev/icons?i=python,ts,java,go,solidity,react,vue,nextjs,tailwind,nestjs,fastapi,spring,nodejs,mysql,postgres,redis,docker,nginx,aws,linux,git)](https://skillicons.dev)

</div>

`Multi-Agent Orchestration (Dify / LangGraph)` `MCP` `RAG (Hybrid Search + Rerank)` `Prompt Engineering (CoT/Few-shot)` `LLM Connection Pooling` `JWT/RBAC` `SSO / Identity Gateway`

---

### 🐍 Contributions

<div align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/HankGrimm/HankGrimm/output/github-contribution-grid-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/HankGrimm/HankGrimm/output/github-contribution-grid-snake.svg" />
  <img alt="GitHub contribution snake" src="https://raw.githubusercontent.com/HankGrimm/HankGrimm/output/github-contribution-grid-snake.svg" />
</picture>
</div>

---

<div align="center">

154+ contributions this year · 23 public repos · Pull Shark 🦈

</div>
