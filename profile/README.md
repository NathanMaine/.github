# Nathan Maine

**Senior Technical Program Manager | AI Systems Builder | Enterprise Delivery**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nathanmaine)
[![Website](https://img.shields.io/badge/Website-000000?style=flat&logo=safari&logoColor=white)](https://nathanmaine.com)
[![Podcast](https://img.shields.io/badge/Podcast-8B5CF6?style=flat&logo=spotify&logoColor=white)](https://podcast.nathanmaine.com)

I deliver enterprise platforms that power critical business outcomes — from identity systems serving 700K users to data platforms unifying 89M records across 28+ sources. I've led $20M+ portfolios at Salesforce with 5/5 CSAT and cut delivery cycles by 67%.

AI systems that solve the problems I've spent a career navigating.

---

## 🎯 Start Here

Three projects that show the core themes: **real-time intelligence**, **agentic AI**, **governance**, and **developer automation**.

| | Project | What It Does |
|--|---------|--------------|
| 🚀 | [**Project Aurora Echo**](https://github.com/NathanMaine/Project-Aurora-Echo) | Real-time audio → transcription → reasoning → structured memory. *Start here.* |
| ✅ | [**Compliance Validation Agent**](https://github.com/NathanMaine/compliance-validation-agent) | Governance-first agent behavior, rule enforcement, structured validation. |
| 🌿 | [**Agentforce Data-Aware Agent**](https://github.com/NathanMaine/Agentforce-Data-Aware-Agent) | Auto-discovers org schema → enforces FLS/sharing → runs safe Apex/Flow. |

---

## 🏢 Enterprise AI Toolkit

Production-grade tools for teams deploying AI agents in enterprise environments. Each solves a real problem I encountered building agentic systems at scale.

| Tool | Problem It Solves | Link |
|------|-------------------|------|
| **Governance Graph Compiler** | Compliance teams spend weeks manually mapping controls to audit evidence. This automates SOC2/SOX control-to-evidence traceability. | [→ Repo](https://github.com/NathanMaine/governance-graph-compiler) |
| **Agentic Evaluation Sandbox** | AI agents are non-deterministic — traditional testing doesn't work. This provides regression testing with scenario batteries and baseline comparisons. | [→ Repo](https://github.com/NathanMaine/agentic-evaluation-sandbox) |
| **Agentic Memory Graph Engine** | Most agents are stateless and forget everything. This adds persistent, queryable memory using RAG and knowledge graphs. | [→ Repo](https://github.com/NathanMaine/agentic-memory-graph-engine) |
| **Self-Healing Agentic Workflows** | AI pipelines crash when APIs timeout or LLMs hallucinate. This adds automatic retries, fallback chains, and circuit breakers. | [→ Repo](https://github.com/NathanMaine/self-healing-agentic-workflows) |

Built with Python. Designed for teams who need **reliability**, **compliance**, and **observability** in their AI deployments.

---

## 🧰 Agent Suite — 5 Runnable Tools

Standalone repos with consistent install flow, CLI entry points, and CI. The fastest hands-on tour.

| Tool | What It Does | Quickstart |
|------|--------------|------------|
| `aes` | Scenario runner with Doer/Judge stubs → evidence + run summary | [→ agentic-evaluation-sandbox](https://github.com/NathanMaine/agentic-evaluation-sandbox#quickstart) |
| `ggc` | Policy Markdown → governance graph exports | [→ governance-graph-compiler](https://github.com/NathanMaine/governance-graph-compiler#quickstart) |
| `amg` | Ingest meeting events → graph memory + explain paths | [→ agentic-memory-graph-engine](https://github.com/NathanMaine/agentic-memory-graph-engine#quickstart) |
| `shaw` | Workflow run with failure → retry → recovery evidence | [→ self-healing-agentic-workflows](https://github.com/NathanMaine/self-healing-agentic-workflows#quickstart) |
| `tea` | Temporal planning by deps/due dates → plan + state | [→ temporal-executive-agent](https://github.com/NathanMaine/temporal-executive-agent#quickstart) |

📦 **Run the whole suite:** [agentic-ai-portfolio](https://github.com/NathanMaine/agentic-ai-portfolio)

---

## 📚 Full Portfolio — 24 Public Projects

### 🧪 Agentic AI Research (10 Core Projects)

# AI Agent Portfolio

**10 repositories. One architecture. Zero black boxes.**

A portfolio of purpose-built AI agents spanning compliance, testing, fairness, documentation, and operational intelligence. Every repo uses deterministic, auditable logic — identical inputs always produce identical outputs. Built for environments where you need to explain every decision to an auditor, not just a user.

---

## 🛡️ The Flagship

### [governed-llm-gateway](https://github.com/NathanMaine/governed-llm-gateway)
**The compliance-first LLM gateway.**

Route LLM requests through a governed endpoint with tamper-evident audit trails, policy-as-code enforcement, and compliance evidence export. The gateway answers the question every CISO asks before approving LLM usage in a regulated environment: *"How do we prove to auditors that every LLM interaction was authorized, logged immutably, and compliant with our policies?"*

`SHA-256 Hash Chain` · `Merkle Tree Verification` · `YAML Policy Engine` · `PII Detection` · `SOC 2 + HIPAA Evidence Packages` · `12 Regulatory Controls Mapped`

---

## ⚡ The Full Portfolio

### Testing & Validation

| # | Repository | What It Does | Distinguishing Feature |
|---|---|---|---|
| 01 | **voice-robustness-testing-agent** | Tests voice/NLU classifiers using structured test sets with pluggable classifier protocols. Regex keyword scoring with tie-breaking catches edge cases that unit tests miss. | 3-state outcome model (PASS / AMBIGUOUS / FAIL) |
| 02 | **architectural-design-review-agent** | Ingests YAML architecture briefs and produces structured reviews via LLM with JSON schema extraction. Dual-mode operation runs with or without an API key. | SHA-256 brief content hashing for evidence integrity |
| 03 | **compliance-validation-agent** | Assesses whether a software change satisfies a compliance checklist. Category-aware keyword matching across 5 domains performs real analysis without requiring an LLM. | Real analysis in stub mode — no LLM required |
| 04 | **agent-perf-test-generator** | Generates structured load test plans from service profiles. Three scenario patterns (steady, burst, soak) with automatic burst threshold relaxation at 1.5x. | Parametric scenario generation with SLO-derived checks |

### Documentation & Knowledge

| # | Repository | What It Does | Distinguishing Feature |
|---|---|---|---|
| 05 | **living-docforce-agent** | Detects documentation drift by comparing entities from source code against docs. Multi-framework support (Flask + Express) with path normalization across conventions. | Version-aware endpoint drift detection — zero LLM dependency |
| 06 | **meeting-memory-companion** | Extracts structured data from meeting notes and answers queries via cascading phrase-based classification across 6 categories with token-overlap scoring. | 6-category query classifier with evidence-backed responses |

### Operations & Intelligence

| # | Repository | What It Does | Distinguishing Feature |
|---|---|---|---|
| 07 | **ai-ops-kpi-pipeline** | ETL pipeline that ingests KPI snapshots and produces aggregated reports. Suffix-based heuristics automatically classify columns — `_total` summed, `latency_` averaged. | Heuristic metric classification — zero external dependencies |
| 08 | **devex-metrics-dashboard** | Evaluates 7 engineering health categories against DORA-aligned thresholds. Signal-counting aggregation prevents single-metric domination. | Signal-counting health aggregation across 7 categories |

### Fairness & Governance

| # | Repository | What It Does | Distinguishing Feature |
|---|---|---|---|
| 09 | **multi-agent-fairness-governor** | Allocates tasks using weighted round-robin with priority ordering and capacity constraints. Weight-expanded rotation ensures exact proportional distribution. | Fully deterministic — skew-ratio fairness metric |

---

## Design Principles

These repos share a common philosophy:

**Deterministic by default.** No hidden randomness, no model drift, no non-reproducible outputs. Given the same inputs, every repo produces the same outputs every time.

**Auditable at every layer.** JSONL evidence logging, hash-chain audit trails, timestamped entries. Every decision can be traced, verified, and explained.

**Minimal dependencies.** Four of the ten repos run on Python's standard library alone. The rest use only well-established, open-source libraries (Click, FastAPI, PyYAML, httpx, Pydantic).

**LLM-optional.** Most repos operate without any LLM calls. Those that support LLM integration also provide a fully functional stub mode for testing, CI/CD, and air-gapped environments.

---

## At a Glance

```
┌──────────────────────────────────────────────────────────────┐
│                    10 REPOS  ·  500+ TESTS                   │
├──────────────────────────────────────────────────────────────┤
│                                                              │
│  🛡️  governed-llm-gateway          Compliance-first gateway │
│  🎙️  voice-robustness-testing      NLU classifier testing   │
│  🏗️  architectural-design-review   Architecture brief review │
│  ✅  compliance-validation          SDLC checklist assessment│
│  📄  living-docforce                Documentation drift       │
│  ⚡  agent-perf-test-generator      Load test plan generation │
│  📊  ai-ops-kpi-pipeline            KPI aggregation pipeline │
│  🧠  meeting-memory-companion       Meeting notes extraction │
│  ⚖️  multi-agent-fairness-governor  Fair task allocation     │
│  📈  devex-metrics-dashboard        DORA metrics engine      │
│                                                              │
├──────────────────────────────────────────────────────────────┤
│  Python  ·  FastAPI  ·  Click CLI  ·  Zero black boxes       │
└──────────────────────────────────────────────────────────────┘
```

---


### 🎙️ Real-Time AI & Meeting Intelligence (5 Projects)

| Project | Description |
|---------|-------------|
| [Project Aurora Echo](https://github.com/NathanMaine/Project-Aurora-Echo) | Real-time meeting copilot |
| [Realtime AI Assistant](https://github.com/NathanMaine/realtime-ai-assistant) | FastAPI template |
| [Streamlit Assistant v4](https://github.com/NathanMaine/realtime-ai-assistant004-stream-lit) | Streamlit + ASR |
| [FastAPI Assistant v3](https://github.com/NathanMaine/realtime-ai-assistant003-fast-api) | Fast backend variant |
| [Streamlit Assistant v2](https://github.com/NathanMaine/realtime-ai-assistant002) | Early ASR → LLM pipeline prototype |

### 🌿 Salesforce / Agentforce (3 Projects)

| Project | Description |
|---------|-------------|
| [Agentforce Data-Aware Agent](https://github.com/NathanMaine/Agentforce-Data-Aware-Agent) | Metadata-aware safe action execution |
| [Dynamic Action](https://github.com/NathanMaine/Agentforce-Dynamic-Action) | Generates Apex actions |
| [Dynamic Action (Invocable)](https://github.com/NathanMaine/Agentforce-Dynamic-Action-Invocable) | Flow-compatible action generator |

### 🧠 Classical AI (2 Projects)

| Project | Description |
|---------|-------------|
| [Backward-Chaining Engine](https://github.com/NathanMaine/LISP-Backward-Chaining-Core-Engine) | Goal-driven inference (Common Lisp) |
| [Car Expert System](https://github.com/NathanMaine/lisp-car-expert-system) | Rule-based troubleshooting (Common Lisp) |

### ♟️ Chess Analysis (2 Projects)

| Project | Description |
|---------|-------------|
| [Chess Analyzer v2](https://github.com/NathanMaine/Chess-Analyzer-v2) | Web-based PGN analysis |
| [Chess Analyzer](https://github.com/NathanMaine/chess-analyzer) | PGN parsing engine (Python) |

### 🎨 Experimental & Creative (2 Projects)

| Project | Description |
|---------|-------------|
| [Thermomix Recipe Genius](https://github.com/NathanMaine/Thermomix-Recipe-Genius) | AI-driven recipe generator |
| [Bongo Cat Monitor Remix](https://github.com/NathanMaine/bongo_cat_monitor_remix) | Animated desktop monitor companion |

---

## 📊 Enterprise Delivery Background

| Domain | Proof Points |
|--------|--------------|
| **Data Platforms** | 89M records, 28+ sources, 95.48% match rates, 99% identity unification |
| **Identity & Security** | 700K users, 200 application SSO, Okta/SAML/OIDC at scale |
| **Program Scale** | $20M+ portfolios, multi-cloud (Sales/Service/Data/Marketing Cloud) |
| **Customer Outcomes** | 5/5 CSAT, "Excellent" on Risk Management and Communication |
| **Process Optimization** | Cycle times cut from 6 weeks → 2 weeks (67% reduction) |

---

## 🎓 Credentials

**MIT** AI/ML Certificate (2024) • **Scrum Alliance** CSM

**Salesforce Certified:** Data Cloud Consultant • Administrator • AI Associate • Financial Services Cloud • Service Cloud • Sales Cloud

---

## 💬 Let's Connect

Exploring roles where enterprise delivery meets AI/ML — particularly in identity, data platforms, and compliance automation.

📧 nmaine@gmail.com • 🔗 [LinkedIn](https://www.linkedin.com/in/nathanmaine) • 🌐 [nathanmaine.com](https://nathanmaine.com) • 📍 Boston, MA (Remote)
