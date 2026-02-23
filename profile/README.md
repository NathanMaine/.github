# Nathan Maine

**Founder, Memoriant Inc. | Senior TPM at Salesforce | Patent-Pending AI Infrastructure**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nathanmaine)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat&logo=huggingface&logoColor=black)](https://huggingface.co/Nathan-Maine)
[![Website](https://img.shields.io/badge/Website-000000?style=flat&logo=safari&logoColor=white)](https://nathanmaine.com)
[![Podcast](https://img.shields.io/badge/Podcast-8B5CF6?style=flat&logo=spotify&logoColor=white)](https://podcast.nathanmaine.com)

I build AI systems for regulated industries — compliance LLMs, governed inference gateways, and evaluation harnesses for autonomous agents. I also manage $20M+ enterprise programs at Salesforce. 12 years delivery, 46 repos.

**Memoriant Inc.** is a Delaware C Corporation building air-gapped compliance AI for the Defense Industrial Base. Patent-pending token governance infrastructure. NASA commitment letter.

---

## Flagship: CMMC Expert

The only CMMC-specific fine-tuned LLM suite in the open-source ecosystem. Four QLoRA models on Qwen2.5-Instruct, trained for $77 total compute, deployed fully air-gapped via Ollama.

| Model | Size | HuggingFace |
|-------|------|-------------|
| cmmc-expert-7b | 5.1 GB | [Nathan-Maine/cmmc-expert-7b](https://huggingface.co/Nathan-Maine/cmmc-expert-7b) |
| cmmc-expert-14b | ~10 GB | [Nathan-Maine/cmmc-expert-14b](https://huggingface.co/Nathan-Maine/cmmc-expert-14b) |
| cmmc-expert-32b | 18.5 GB | [Nathan-Maine/cmmc-expert-32b](https://huggingface.co/Nathan-Maine/cmmc-expert-32b) |
| cmmc-expert-72b | 44.2 GB | [Nathan-Maine/cmmc-expert-72b](https://huggingface.co/Nathan-Maine/cmmc-expert-72b) |

13,434 training examples from 5 government sources. Frameworks: CMMC 2.0, NIST 800-171 Rev 2/3, 800-53 Rev 5, HIPAA, DFARS.

| Repository | What It Does | Tests |
|------------|-------------|-------|
| [**cmmc-compliance-ai-model**](https://github.com/NathanMaine/cmmc-compliance-ai-model) | The 4 fine-tuned models + training pipeline | Published on HuggingFace |
| [**governed-llm-gateway**](https://github.com/NathanMaine/governed-llm-gateway) | SHA-256 hash-chain audit trails, YAML policy-as-code, PII detection | 103/103 passing |
| [**garak-compliance-probes**](https://github.com/NathanMaine/garak-compliance-probes) | Adversarial probes for NVIDIA garak (PR #1619 — 20 files, 1,599 lines) | Contributed upstream |

---

## Agentic Evaluation Sandbox

Holdout scenario evaluation harness for AI agents. Created **December 16, 2025**.

Scenarios are stored *outside* the codebase — agents can't game what they can't see. The architecture uses Doer / Judge / Adversary / Observer roles with probabilistic satisfaction scoring (threshold ≥ 0.85) and append-only JSONL audit trails with integrity hashes.

| Repository | What It Does |
|------------|-------------|
| [**agentic-evaluation-sandbox**](https://github.com/NathanMaine/agentic-evaluation-sandbox) | Holdout scenario evaluator with 4-role architecture |
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

---

## Additional Projects

<details>
<summary><strong>Real-Time AI & Meeting Intelligence</strong> (5 projects)</summary>

| Project | Description |
|---------|-------------|
| [Project Aurora Echo](https://github.com/NathanMaine/Project-Aurora-Echo) | Real-time meeting copilot (FastAPI + WebSocket + faster-whisper) |
| [Aurora Echo v2.0](https://github.com/NathanMaine/Project-Aurora-Echo-v2.0) | Enhanced variant |
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
<summary><strong>Classical AI & Other</strong> (6 projects)</summary>

| Project | Description |
|---------|-------------|
| [Backward-Chaining Engine](https://github.com/NathanMaine/LISP-Backward-Chaining-Core-Engine) | Goal-driven inference (Common Lisp) |
| [Car Expert System](https://github.com/NathanMaine/lisp-car-expert-system) | Rule-based troubleshooting (Common Lisp) |
| [Chess Analyzer v2](https://github.com/NathanMaine/Chess-Analyzer-v2) | Web-based PGN analysis (React + TypeScript) |
| [Chess Analyzer](https://github.com/NathanMaine/chess-analyzer) | PGN parsing engine (Python + Stockfish) |
| [Thermomix Recipe Genius](https://github.com/NathanMaine/Thermomix-Recipe-Genius) | AI recipe generator (Next.js + FastAPI) |
| [Bongo Cat Monitor](https://github.com/NathanMaine/bongo_cat_monitor_remix) | ESP32 desk companion with TFT display |

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

**Memoriant Inc.** — Delaware C Corporation — [memoriant.ai](https://memoriant.ai)

nmaine@gmail.com · [LinkedIn](https://www.linkedin.com/in/nathanmaine) · [nathanmaine.com](https://nathanmaine.com) · [HuggingFace](https://huggingface.co/Nathan-Maine)
