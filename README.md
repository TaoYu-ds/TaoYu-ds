# TaoYu

**Agent 应用开发** · Building LLM systems that are evaluable, observable, and degradable.

我关心的不是「怎么让模型回答得更像人」，而是「怎么让它在出错时还能被定位、被度量、被兜住」。

---

## 三个项目，三个工程切面

### [AgentRig](https://github.com/TaoYu-ds/AgentRig) · 本地 Agent Runtime

> 一个 Agent Runtime 最少需要哪些骨架？

把「编码 Agent」拆成可替换的部件，而不是堆成一个巨型 prompt：工具调用、权限确认、会话记忆折叠、Skills 自进化、MCP、子 Agent。

`Python` · `MCP` · `Tool Calling` · `Memory` · `MIT`

### [TutorMesh](https://github.com/TaoYu-ds/TutorMesh) · 在线教育多 Agent 学习辅导

> 垂直场景里，多 Agent 怎么落地又不失控？

三路意图融合（LLM + Embedding + Pattern）→ 主辅 Agent 路由 → BM25 与向量混合检索 → 分层记忆与学习画像 → 转人工。
自建 57 条检索评测集，Recall@1 从 15.8% 提升到 40.4%，MRR 0.19 → 0.63。

`FastAPI` · `LangGraph` · `ChromaDB` · `Redis` · `Vue 3` · `Docker`

### [QueryPilot](https://github.com/TaoYu-ds/QueryPilot) · 自然语言问数工作台

> 让业务敢用 NL2SQL，需要补哪些东西？

字段级 Schema 混合检索先把候选字段缩小，LangGraph 负责澄清与重试，MCP 工具运行时约束可执行动作，DuckDB 负责真实执行。
57 条用例覆盖单表、多表、指标口径与澄清分支。

`LangGraph` · `DuckDB` · `MCP` · `Text-to-SQL` · `Evaluation`

---

## 技术栈

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&amp;logo=python&amp;logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&amp;logo=fastapi&amp;logoColor=white" alt="FastAPI" />
  <img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square" alt="LangGraph" />
  <img src="https://img.shields.io/badge/MCP-6E56CF?style=flat-square" alt="MCP" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&amp;logo=redis&amp;logoColor=white" alt="Redis" />
  <img src="https://img.shields.io/badge/ChromaDB-FF6B6B?style=flat-square" alt="ChromaDB" />
  <img src="https://img.shields.io/badge/DuckDB-FFF000?style=flat-square&amp;logoColor=black" alt="DuckDB" />
  <img src="https://img.shields.io/badge/Vue_3-4FC08D?style=flat-square&amp;logo=vuedotjs&amp;logoColor=white" alt="Vue 3" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&amp;logo=docker&amp;logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&amp;logo=prometheus&amp;logoColor=white" alt="Prometheus" />
</p>

---

## 关注方向

- **评测**：LLM-as-Judge、回归基线、检索指标（Recall / MRR / NDCG），不把「跑通」当成「做好」
- **成本**：意图分层、TTL 缓存、按需检索、上下文压缩，让贵的调用只发生在必要的地方
- **故障**：超时、熔断、降级、幂等与不可重放标记，失败要能被解释
- **MCP**：客户端与服务端双向集成，工具治理与接入分层
- **个性化**：per-user LoRA 与 agent memory 的「写入—管理—读取」循环

---

<div align="center">
  <sub>Open to Agent engineering roles · 2027 campus recruiting</sub>
</div>
