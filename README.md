<div align="center">

# Hank Grimm · 韩广宁

**Agent / AI Engineering · CS (创新人才实验班) @ Guangzhou College of Commerce · 2023–2027**

Building AI-native full-stack systems — from streaming runtimes & Agent event channels to security-hardened backend integrations.

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
- **Provincial First Prize, Guangdong "Maker Cube Robot" Competition (广东省创客魔方机器人比赛 · 高中组)** `高中`

---

### 💼 Experience

**AI Full-Stack Intern · Baidu (China) Co., Ltd. Guangzhou Branch** `2026.07 – Present`

GenFlow (pnpm monorepo multi-device AI framework) runtime + AICRM customer-data pipeline.

**GenFlow — 多端 AI 应用框架（AI 对话 / PPT 生成 · 一次编写、四端交付）**

- Unified streaming runtime: business calls `useSseStream(runtime).start({prompt})`; the platform package injects SSE (PC `EventSource` / NA JSBridge duplex / WAP weak-network fallback) and normalizes raw frames before handing off to message components
- Agent-oriented event channel: `runtime.eventBus` decouples SSE producers from message/state/debug consumers; plugins register via `runtime.use(plugin)` on the Chat/PPT lifecycle
- Cross-platform isolation: shared logic sinks to the common layer with per-platform providers absorbing device diffs; dual vue2/vue3 entries switch by preset; playground mocks the AI stream for 4-device side-by-side debugging

**AICRM — 企微 × One CRM 客户主数据打通 · 加好友事件驱动链路**

- `销服 BI → dbt 数仓 → FastAPI（/v1 / /skill / /internal）→ Web + AI 技能`; owned the customer master-data & event-integration backend
- Deterministic matching (phone → company full/short name) under a "never mis-bind" policy; live `getWeChatRel` re-check before write (cache never used as write source); 3/hour + 30-min cooldown
- Idempotent add-friend events (202 async) with `FOR UPDATE SKIP LOCKED` + 120s-lease workers; snapshot table + scheduled refresh cut `GET /customers` 32s → 0.1–0.3s

**AI/LLM Engineering Intern · Guangzhou Xin'an Data Co., Ltd.** `2026.04 – 2026.07`

Built Multi-Agent document review pipelines for enterprise brand & KPI compliance systems.

- Preprocessed stamped scans (OpenCV de-stamp/de-watermark + CLAHE) before `PaddleOCR`; fused title (0.6) + full-text (0.4) vectors; hierarchical Markdown chunking + Hybrid Search + Reranker on `Milvus` — QA accuracy **60% → 88%** on a 1,000-metric eval set
- Built the "review → suggestion → revision" loop: Dify multi-node workflow, 7 intent-routed parallel retrieval, 5-element structured verdicts; similarity-aided report ingestion to avoid duplicate archives
- Provider-agnostic async LLM connection pool (rate-limit, exponential backoff, retry, streaming); multi-arch ARM64 images via `docker buildx` across 13 services with `request_id + task_id` tracing

**Founder / Full-Stack Developer · Guangzhou Kangxiaomiao Smart Technology Co., Ltd. (BoBaCarry)** `2025.09 – 2026.04`

Built a shared smart-follow-cart platform end-to-end, from WeChat Mini Program to production deployment.

- `Node.js + Express` backend with `MySQL + Redis` (**<50ms** response latency); `Vue 3 + Element Plus` ops console; WeChat Mini Program (device binding / live status / history / login)
- Defined MQTT device protocol + built a device simulator before hardware arrived; fixed a reconnect-without-resubscribe bug; virtual queue + structured concurrency for batch dispatch
- Intent-routed customer-service loop (query / urge / repair) with tool calls; token-cost attribution via `LangSmith` trace normalization; Nginx + HTTPS + PM2 + COS with circuit-breaker & idempotency

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
