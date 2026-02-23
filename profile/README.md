# Nathan Maine

**Senior Technical Program Manager | AI Systems Builder | 12+ Years Enterprise Delivery**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nathanmaine)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat&logo=huggingface&logoColor=black)](https://huggingface.co/Nathan-Maine)
[![Website](https://img.shields.io/badge/Website-000000?style=flat&logo=safari&logoColor=white)](https://nathanmaine.com)
[![Podcast](https://img.shields.io/badge/Podcast-8B5CF6?style=flat&logo=spotify&logoColor=white)](https://podcast.nathanmaine.com)

I build the AI systems I've spent a career learning to manage — compliance LLMs, governed inference gateways, evaluation harnesses for autonomous agents, and patent-pending token governance infrastructure. 12 years enterprise delivery across identity platforms (700K users), data unification (89M records, 95.48% match rates), and $20M+ multi-cloud programs. 49 repos.

---

## CMMC Expert Platform (v1.5.0)

The only CMMC-specific fine-tuned LLM suite in the open-source ecosystem. Four models (7B–72B) trained for $77 total compute, deployed fully air-gapped via Ollama. The platform implements 27 CMMC controls across 5 families (AC, AU, IA, SC, SI) plus 3 DFARS clauses.

| Model | Size | HuggingFace |
|-------|------|-------------|
| cmmc-expert-7b | 5.1 GB | [Nathan-Maine/cmmc-expert-7b](https://huggingface.co/Nathan-Maine/cmmc-expert-7b) |
| cmmc-expert-14b | ~10 GB | [Nathan-Maine/cmmc-expert-14b](https://huggingface.co/Nathan-Maine/cmmc-expert-14b) |
| cmmc-expert-32b | 18.5 GB | [Nathan-Maine/cmmc-expert-32b](https://huggingface.co/Nathan-Maine/cmmc-expert-32b) |
| cmmc-expert-72b | 44.2 GB | [Nathan-Maine/cmmc-expert-72b](https://huggingface.co/Nathan-Maine/cmmc-expert-72b) |

**690 total tests** across a three-tier architecture (550 internal + 140 Dark Factory behavioral scenarios):

| Repository | What It Does | Tests |
|------------|-------------|-------|
| [**governed-llm-gateway**](https://github.com/NathanMaine/governed-llm-gateway) | SHA-256 hash-chain audit trails, YAML policy-as-code, PII/CUI detection, compliance evidence export | 134 passing |
| [**cmmc-compliance-ai-model**](https://github.com/NathanMaine/cmmc-compliance-ai-model) | The 4 fine-tuned models + training pipeline | Published on HuggingFace |
| [**garak-compliance-probes**](https://github.com/NathanMaine/garak-compliance-probes) | Adversarial probes for NVIDIA garak ([PR #1619](https://github.com/NVIDIA/garak/pull/1619) — 20 files, 1,599 lines) | Contributed upstream |
| [**garak**](https://github.com/NathanMaine/garak) | Fork of NVIDIA/garak with compliance probe development branch | PR source |

The governed-llm-gateway is the only LLM gateway with tamper-evident audit trails (SHA-256 hash-chain), policy-as-code enforcement, and built-in PII/CUI detection — capabilities absent from LiteLLM, Portkey, and TensorZero. Every user message traverses an 11-step audited inference pipeline enforced by code, not configuration.

---

## Dark Factory Testing & Agentic Evaluation

**140 black-box behavioral scenarios** in a physically separate holdout repository. The AI agents that build the platform never see these tests — an agent cannot game what it cannot see. Docker digital twin with mock Ollama for deterministic, zero-GPU execution. Latest sweep: 130 passed, 3 real platform findings discovered.

This architecture independently converged with [StrongDM's Software Factory](https://factory.strongdm.ai) pattern (published February 2026). The [Agentic Evaluation Sandbox](https://github.com/NathanMaine/agentic-evaluation-sandbox) formalizing this pattern was created **December 2025**, predating their publication.

| Repository | What It Does |
|------------|-------------|
| [**agentic-evaluation-sandbox**](https://github.com/NathanMaine/agentic-evaluation-sandbox) | Holdout scenario evaluator — Doer/Judge/Adversary/Observer roles, probabilistic scoring, append-only audit trails. Created Dec 2025. |
| [**governance-graph-compiler**](https://github.com/NathanMaine/governance-graph-compiler) | Policy Markdown → directed acyclic graph for compliance traceability |

**Run the full suite:** [agentic-ai-portfolio](https://github.com/NathanMaine/agentic-ai-portfolio) — AES · GGC · AMG · SHAW · TEA

---

## Deterministic Agent Suite

Purpose-built agents using deterministic, auditable logic — identical inputs always produce identical outputs. Zero black boxes.

### Testing & Validation

| Repository | What It Does | Key Feature |
|---|---|---|
| [voice-robustness-testing-agent](https://github.com/NathanMaine/voice-robustness-testing-agent) | Tests voice/NLU classifiers with pluggable protocols | 3-state outcome model |
| [architectural-design-review-agent](https://github.com/NathanMaine/architectural-design-review-agent) | YAML architecture briefs → structured LLM reviews | SHA-256 evidence integrity |
| [compliance-validation-agent](https://github.com/NathanMaine/compliance-validation-agent) | Multi-framework compliance checklists (SOX, SOC2, NIST, CMMC) | Zero LLM dependency |
| [agent-perf-test-generator](https://github.com/NathanMaine/agent-perf-test-generator) | Load test plans (steady/burst/soak) from service profiles | SLO-derived checks |

### Memory, Planning & Recovery

| Repository | What It Does | Key Feature |
|---|---|---|
| [agentic-memory-graph-engine](https://github.com/NathanMaine/agentic-memory-graph-engine) | Persistent, queryable agent memory using RAG + knowledge graphs | explain() paths |
| [self-healing-agentic-workflows](https://github.com/NathanMaine/self-healing-agentic-workflows) | Automatic retries, fallback chains, circuit breakers | Deterministic recovery |
| [temporal-executive-agent](https://github.com/NathanMaine/temporal-executive-agent) | Dependency-ordered planning with state tracking | Temporal planning |
| [multi-agent-fairness-governor](https://github.com/NathanMaine/multi-agent-fairness-governor) | Weighted round-robin task allocation with capacity constraints | Skew-ratio metric |

### Documentation & Operations

| Repository | What It Does | Key Feature |
|---|---|---|
| [living-docforce-agent](https://github.com/NathanMaine/living-docforce-agent) | Detects documentation drift across Flask + Express | Version-aware |
| [meeting-memory-companion](https://github.com/NathanMaine/meeting-memory-companion) | Extracts structured meeting data via 6-category classification | Token-overlap scoring |
| [ai-ops-kpi-pipeline](https://github.com/NathanMaine/ai-ops-kpi-pipeline) | ETL with suffix-based heuristic aggregation | Zero dependencies |
| [devex-metrics-dashboard](https://github.com/NathanMaine/devex-metrics-dashboard) | 7 DORA-aligned health categories | Signal-counting aggregation |
| [agent-zero-dashboard](https://github.com/NathanMaine/agent-zero-dashboard) | Monitoring dashboard for Agent Zero autonomous AI framework | Real-time state visualization |

---

## Additional Projects

<details>
<summary><strong>Real-Time AI & Meeting Intelligence</strong> (5 projects)</summary>

| Project | Description |
|---------|-------------|
| [Project Aurora Echo](https://github.com/NathanMaine/Project-Aurora-Echo) | Real-time meeting copilot (FastAPI + WebSocket + faster-whisper) |
| [Aurora Echo v2.0](https://github.com/NathanMaine/Project-Aurora-Echo-v2.0) | NVIDIA-accelerated variant |
| [FastAPI Assistant v3](https://github.com/NathanMaine/realtime-ai-assistant003-fast-api) | GPU-accelerated backend |
| [Streamlit Assistant v4](https://github.com/NathanMaine/realtime-ai-assistant004-stream-lit) | Streamlit + ASR |
| [Realtime AI Assistant](https://github.com/NathanMaine/realtime-ai-assistant) | FastAPI template |

</details>

<details>
<summary><strong>Salesforce / Agentforce</strong> (3 projects)</summary>

| Project | Description |
|---------|-------------|
| [Agentforce Data-Aware Agent](https://github.com/NathanMaine/Agentforce-Data-Aware-Agent) | Auto-discovers org schema → enforces FLS/sharing → runs safe Apex/Flow |
| [Dynamic Action](https://github.com/NathanMaine/Agentforce-Dynamic-Action) | Natural language → generated Apex actions |
| [Dynamic Action (Invocable)](https://github.com/NathanMaine/Agentforce-Dynamic-Action-Invocable) | Flow-compatible action generator |

</details>

<details>
<summary><strong>Classical AI & Other</strong> (7 projects)</summary>

| Project | Description |
|---------|-------------|
| [Backward-Chaining Engine](https://github.com/NathanMaine/LISP-Backward-Chaining-Core-Engine) | Goal-driven inference (Common Lisp) |
| [Car Expert System](https://github.com/NathanMaine/lisp-car-expert-system) | Rule-based troubleshooting (Common Lisp) |
| [Chess Analyzer v2](https://github.com/NathanMaine/Chess-Analyzer-v2) | Web-based PGN analysis (React + TypeScript) |
| [Chess Analyzer](https://github.com/NathanMaine/chess-analyzer) | PGN parsing engine (Python + Stockfish) |
| [Thermomix Recipe Genius](https://github.com/NathanMaine/Thermomix-Recipe-Genius) | AI recipe generator (Next.js + FastAPI) |
| [Bongo Cat Monitor](https://github.com/NathanMaine/bongo_cat_monitor_remix) | ESP32 desk companion with TFT display |
| [GitHub Avatar Rotator](https://github.com/NathanMaine/Github-Avatar-Rotator) | Automated GitHub avatar rotation |

</details>

---

## Background

| Domain | Proof Points |
|--------|--------------|
| **Data Platforms** | 89M records → 45.9M unified profiles, 95.48% match rate, 99% identity unification |
| **Identity & Security** | 700,000-user Okta deployment, 200 application SSO (SAML/OIDC) |
| **Compliance** | SOX, SOC2, HIPAA, NIST 800-171, CMMC, FedRAMP adjacency |
| **Program Delivery** | $20M+ multi-cloud portfolios, 5/5 CSAT, "Excellent" risk management |
| **Process** | 6 weeks → 2 weeks onboarding cycle (67% reduction) |

**MIT** AI/ML Certificate · **Salesforce:** Data Cloud Consultant · Administrator · AI Associate · **Scrum:** CSM

---

nmaine@gmail.com · [LinkedIn](https://www.linkedin.com/in/nathanmaine) · [nathanmaine.com](https://nathanmaine.com) · [HuggingFace](https://huggingface.co/Nathan-Maine)
