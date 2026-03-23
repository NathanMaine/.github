# Nathan Maine

**Senior Technical Program Manager | Security Compliance & AI Governance | Enterprise Delivery**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nathanmaine)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat&logo=huggingface&logoColor=black)](https://huggingface.co/Nathan-Maine)
[![Website](https://img.shields.io/badge/Website-000000?style=flat&logo=safari&logoColor=white)](https://nathanmaine.com)
[![Podcast](https://img.shields.io/badge/Podcast-8B5CF6?style=flat&logo=spotify&logoColor=white)](https://podcast.nathanmaine.com)

I build governance structures and accountability models that make compliance scale across federated engineering teams without creating drag. 13+ years leading security, compliance, and enterprise platform programs across multiple independent organizations. $20M+ portfolios, 700K-user identity systems, consecutive 5/5 CSAT across different client organizations.

Now building AI-enabled compliance tooling to automate what most teams still do manually: evidence collection, control mapping, and audit preparation.

---

## 🔒 Security Compliance & AI Governance

Tools for scaling compliance across federated product teams, automating audit evidence, and testing AI systems for regulatory risk.

| Project | What It Solves | Link |
| --- | --- | --- |
| **garak Compliance Probes** | LLMs in regulated industries fabricate citations, leak PII, and bypass controls. 4 probes, 6 detectors, 80 adversarial prompts submitted to NVIDIA's garak framework (PR #1619, 20 files, 1,599 lines). | [→ Repo](https://github.com/NathanMaine/garak-compliance-probes) |
| **Governance Graph Compiler** | Compliance teams spend weeks manually mapping controls to audit evidence. This compiles policy-as-code into DAGs for deterministic, auditable evaluation. SOC2/SOX/ISO control traceability automated. | [→ Repo](https://github.com/NathanMaine/governance-graph-compiler) |
| **Compliance Validation Agent** | Governance-first agent that validates workflows against compliance rules, generates pass/fail audit trails, and logs structured evidence. | [→ Repo](https://github.com/NathanMaine/compliance-validation-agent) |
| **Governed LLM Gateway** | Compliance-first AI gateway with policy enforcement, SHA-256 tamper-evident audit trails, rate limiting, and cost telemetry. 103 tests. | [→ Repo](https://github.com/NathanMaine/governed-llm-gateway) |

---

## 🏗️ CMMC Compliance AI Models

Four fine-tuned LLMs (7B–72B) trained on 18,000+ regulatory examples (ISO, NIST, SOC, HIPAA, DFARS). Air-gapped deployment via Ollama. 708 tests across three tiers including 140 blind holdout scenarios. 27 CMMC controls across 5 families (AC, AU, IA, SC, SI).

| Model | Size | HuggingFace |
|-------|------|-------------|
| cmmc-expert-7b | 5.1 GB | [Nathan-Maine/cmmc-expert-7b](https://huggingface.co/Nathan-Maine/cmmc-expert-7b) |
| cmmc-expert-14b | ~10 GB | [Nathan-Maine/cmmc-expert-14b](https://huggingface.co/Nathan-Maine/cmmc-expert-14b) |
| cmmc-expert-32b | 18.5 GB | [Nathan-Maine/cmmc-expert-32b](https://huggingface.co/Nathan-Maine/cmmc-expert-32b) |
| cmmc-expert-72b | 44.2 GB | [Nathan-Maine/cmmc-expert-72b](https://huggingface.co/Nathan-Maine/cmmc-expert-72b) |

| Repository | What It Does |
|---|---|
| [**cmmc-compliance-ai-model**](https://github.com/NathanMaine/cmmc-compliance-ai-model) | 4 fine-tuned LLMs for CMMC 2.0, NIST 800-171, HIPAA. Published on Hugging Face. |
| [**garak-compliance-probes**](https://github.com/NathanMaine/garak-compliance-probes) | 4 probes + 6 detectors for NVIDIA's garak vulnerability scanner — [PR #1619](https://github.com/NVIDIA/garak/pull/1619) |
| [**governed-llm-gateway**](https://github.com/NathanMaine/governed-llm-gateway) | Policy-as-code LLM gateway with SHA-256 tamper-evident audit trails |
| [**governance-graph-compiler**](https://github.com/NathanMaine/governance-graph-compiler) | Converts governance policy Markdown into enforceable directed acyclic graphs |

---

## ⛳ Active: OpenAI Parameter Golf Competition

Training the best LLM in 16MB on 8×H100s. Three progressive submissions in 4 days, 40+ experiments, ~$150 total compute:

| Submission | val_bpb | Techniques |
|---|---|---|
| [PR #273](https://github.com/openai/parameter-golf/pull/273) | 1.1575 | Int6 QAT + SmearGate + SWA |
| [PR #385](https://github.com/openai/parameter-golf/pull/385) | 1.1488 | + WD tuning + SWA optimization (3-seed verified) |
| [PR #406](https://github.com/openai/parameter-golf/pull/406) | **1.1287** | + XSA4 + EMA + Self-Distillation TTT (3-seed verified) |

*Active competition: Mar 18 – Apr 30, 2026.*

---

## 🤖 Agentic AI Systems

Purpose-built components for agent memory, recovery, planning, and coordination. Deterministic and auditable.

| Repository | What It Does |
|---|---|
| [**agentic-evaluation-sandbox**](https://github.com/NathanMaine/agentic-evaluation-sandbox) | Doer/Judge holdout scenario evaluation harness |
| [**blind-scenario-testing**](https://github.com/NathanMaine/blind-scenario-testing) | Blind behavioral testing of live API systems — 151 tests |
| [**agentic-memory-graph-engine**](https://github.com/NathanMaine/agentic-memory-graph-engine) | Graph-based memory with explain() reasoning traces |
| [**self-healing-agentic-workflows**](https://github.com/NathanMaine/self-healing-agentic-workflows) | Retry logic, fallback chains, circuit breakers for agent tasks |
| [**temporal-executive-agent**](https://github.com/NathanMaine/temporal-executive-agent) | Dependency-ordered planning and execution with state tracking |
| [**multi-agent-fairness-governor**](https://github.com/NathanMaine/multi-agent-fairness-governor) | Weighted round-robin allocation with skew-ratio detection |
| [**agentic-workflow-simplifier**](https://github.com/NathanMaine/agentic-workflow-simplifier) | Multi-agent workflows as directed graphs |
| [**mcp-conversational-data-agent**](https://github.com/NathanMaine/mcp-conversational-data-agent) | MCP server exposing database/CRM/ticket tools to LLMs |
| [**semantic-test-coverage-agent**](https://github.com/NathanMaine/semantic-test-coverage-agent) | AST-based source/test scanner that finds untested code paths |

📦 **Run the whole suite:** [agentic-ai-portfolio](https://github.com/NathanMaine/agentic-ai-portfolio)

---

## 🧠 Expert Knowledge Systems

AI-queryable knowledge bases from expert content. Production system running 130,000+ searchable chunks across 36+ domain experts with GPU-accelerated ingestion and cross-encoder reranking.

| Repository | What It Does |
|---|---|
| [**rah-qdrant-integration**](https://github.com/NathanMaine/rah-qdrant-integration) | Qdrant vector search integration — Docker, CLI tools, cross-platform |

---

## 🎙️ Real-Time AI & Meeting Intelligence

| Repository | What It Does |
|---|---|
| [**Project-Aurora-Echo**](https://github.com/NathanMaine/Project-Aurora-Echo) | AI meeting copilot — real-time transcription, speaker diarization, structured summaries. [v2.0](https://github.com/NathanMaine/Project-Aurora-Echo-v2.0): GPU acceleration |
| [**realtime-ai-assistant**](https://github.com/NathanMaine/realtime-ai-assistant) | Four iterations: [vanilla](https://github.com/NathanMaine/realtime-ai-assistant) → [v2](https://github.com/NathanMaine/realtime-ai-assistant002) → [FastAPI](https://github.com/NathanMaine/realtime-ai-assistant003-fast-api) → [Streamlit](https://github.com/NathanMaine/realtime-ai-assistant004-stream-lit) |
| [**memoriant-ops-bot**](https://github.com/NathanMaine/memoriant-ops-bot) | Multi-provider AI agent remote control via Telegram & Matrix (Claude Code + Codex CLI + Gemini CLI) |

---

## 🎯 AI Model Serving

| Repository | What It Does |
|---|---|
| [**el-barto-serve**](https://github.com/NathanMaine/el-barto-serve) | OpenAI-compatible server for mask-diffusion code LLM. Auto-patches Flash Attention for Blackwell GPUs. |

---

## ☁️ Salesforce / Agentforce

| Repository | What It Does |
|---|---|
| [**Agentforce-Data-Aware-Agent**](https://github.com/NathanMaine/Agentforce-Data-Aware-Agent) | Schema-aware AI agent with FLS/sharing enforcement |
| [**Agentforce-Dynamic-Action**](https://github.com/NathanMaine/Agentforce-Dynamic-Action) | Natural language → generated Apex actions |
| [**Agentforce-Dynamic-Action-Invocable**](https://github.com/NathanMaine/Agentforce-Dynamic-Action-Invocable) | Flow/Einstein Copilot/REST wrapper for dynamic actions |

---

<details>
<summary><strong>Developer Experience & Operations</strong> (8 projects)</summary>

| Repository | What It Does |
|---|---|
| [**architectural-design-review-agent**](https://github.com/NathanMaine/architectural-design-review-agent) | LLM-powered architecture review from YAML briefs |
| [**living-docforce-agent**](https://github.com/NathanMaine/living-docforce-agent) | Documentation drift detection — code vs docs comparison |
| [**meeting-memory-companion**](https://github.com/NathanMaine/meeting-memory-companion) | Structured extraction from meeting notes |
| [**devex-metrics-dashboard**](https://github.com/NathanMaine/devex-metrics-dashboard) | DORA-aligned developer experience health indicators |
| [**devex-env-bootstrap-agent**](https://github.com/NathanMaine/devex-env-bootstrap-agent) | Auto-generates dev environment setup scripts |
| [**ai-ops-kpi-pipeline**](https://github.com/NathanMaine/ai-ops-kpi-pipeline) | ETL pipeline for AI operations metrics |
| [**ai-deployment-experience-bot**](https://github.com/NathanMaine/ai-deployment-experience-bot) | Slack bot for deploy/rollback/status via chat |
| [**agent-zero-dashboard**](https://github.com/NathanMaine/agent-zero-dashboard) | Real-time monitoring dashboard for Agent Zero |

</details>

<details>
<summary><strong>Classical AI & Side Projects</strong> (7 projects)</summary>

| Repository | What It Does |
|---|---|
| [**LISP-Backward-Chaining-Core-Engine**](https://github.com/NathanMaine/LISP-Backward-Chaining-Core-Engine) | Common Lisp expert system with backward chaining and certainty scores |
| [**lisp-car-expert-system**](https://github.com/NathanMaine/lisp-car-expert-system) | Rule-based car troubleshooting with forward chaining inference |
| [**Chess-Analyzer-v2**](https://github.com/NathanMaine/Chess-Analyzer-v2) | React + TypeScript chess analysis with Chess.com import |
| [**chess-analyzer**](https://github.com/NathanMaine/chess-analyzer) | Desktop Python chess analyzer with Stockfish + AI commentary |
| [**Thermomix-Recipe-Genius**](https://github.com/NathanMaine/Thermomix-Recipe-Genius) | AI recipe generator for Thermomix TM6 (Gemini + Grok) |
| [**bongo_cat_monitor_remix**](https://github.com/NathanMaine/bongo_cat_monitor_remix) | ESP32 animated desk buddy — CPU/RAM/WPM monitor |
| [**Github-Avatar-Rotator**](https://github.com/NathanMaine/Github-Avatar-Rotator) | Automated GitHub avatar rotation via API |

</details>

---

## 📊 Enterprise Delivery Background

| Domain | Proof Points |
| --- | --- |
| **Security & Identity** | 700K users, 200 application SSO, Okta/SAML/OIDC across federated business divisions |
| **Compliance Governance** | SOC2/SOX-aligned evidence capture, audit preparation, accountability models across independent orgs |
| **Data Platforms** | 89M records, 28+ independent source-system owners, 95.48% match rates, 99% identity unification |
| **Program Scale** | $20M+ portfolios across multiple client organizations, multi-cloud (Sales/Service/Data/Marketing Cloud) |
| **Customer Outcomes** | Consecutive 5/5 CSAT across different organizations, Excellent on Risk Management and Communication |
| **Process Optimization** | Cycle times cut from 6 weeks → 2 weeks (67% reduction) |

---

Plus private repositories covering compliance training data pipelines, podcast production platform, and infrastructure automation.

**MIT** AI/ML Certificate · **Salesforce:** Data Cloud Consultant · Administrator · AI Associate · **Scrum:** CSM · **NVIDIA Inception** Member

📧 nmaine@gmail.com · 🔗 [LinkedIn](https://www.linkedin.com/in/nathanmaine) · 🌐 [nathanmaine.com](https://nathanmaine.com) · 🤗 [HuggingFace](https://huggingface.co/Nathan-Maine) · 📍 Houston, TX
