# Nathan Maine

**Senior Technical Program Manager | AI Systems Builder | NVIDIA Inception Member**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nathanmaine)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat&logo=huggingface&logoColor=black)](https://huggingface.co/Nathan-Maine)
[![Website](https://img.shields.io/badge/Website-000000?style=flat&logo=safari&logoColor=white)](https://nathanmaine.com)
[![Memoriant](https://img.shields.io/badge/Memoriant.ai-6366f1?style=flat&logo=safari&logoColor=white)](https://memoriant.ai)
[![Podcast](https://img.shields.io/badge/Podcast-8B5CF6?style=flat&logo=spotify&logoColor=white)](https://podcast.nathanmaine.com)

I build AI systems I've spent a career learning to manage — compliance LLMs, expert knowledge platforms, governed inference gateways (patent pending), and behavioral AI voice synthesis. 12 years enterprise delivery across identity platforms (700K users), data unification (89M records, 95.48% match rates), and $20M+ multi-cloud programs. NVIDIA Inception member running production AI on DGX Spark.

---

## 🔥 Active Projects & Challenges

<table>
<tr>
<td width="80" align="center"><a href="https://github.com/NathanMaine/memoriant-ops-bot"><img src="https://raw.githubusercontent.com/NathanMaine/memoriant-ops-bot/main/docs/images/mops-logo.jpeg" width="64"></a></td>
<td><a href="https://github.com/NathanMaine/memoriant-ops-bot"><strong>MOPS</strong></a> — Multi-provider AI agent remote control via Telegram & Matrix. Claude Code + Codex CLI + Gemini CLI from your phone. Open-source alternative to Claude Dispatch — released 5 days before Anthropic shipped theirs. <em>Free, MIT licensed.</em></td>
</tr>
<tr>
<td width="80" align="center">⛳</td>
<td><a href="https://github.com/openai/parameter-golf"><strong>Parameter Golf</strong></a> — OpenAI Model Craft Challenge. Train the best LLM in 16MB on 8×H100s. Three progressive submissions in 4 days, 40+ experiments, ~$150 total compute:<br><br>
<table>
<tr><th>Submission</th><th>val_bpb</th><th>Techniques</th></tr>
<tr><td><a href="https://github.com/openai/parameter-golf/pull/273">PR #273</a></td><td>1.1575</td><td>Int6 QAT + SmearGate + SWA</td></tr>
<tr><td><a href="https://github.com/openai/parameter-golf/pull/385">PR #385</a></td><td>1.1488</td><td>+ WD tuning + SWA optimization (3-seed verified)</td></tr>
<tr><td><a href="https://github.com/openai/parameter-golf/pull/406">PR #406</a></td><td><strong>1.1287</strong></td><td>+ XSA4 + EMA + Self-Distillation TTT (3-seed verified)</td></tr>
</table>
The leaderboard is highly competitive and evolving rapidly — scores improve daily as the community discovers and stacks new techniques. Currently exploring custom Triton GPU kernels and Flash Attention 3 builds for further optimization. <em>Active competition: Mar 18 – Apr 30, 2026.</em></td>
</tr>
</table>

---

## 🏗️ Flagship: CMMC Compliance AI Platform

The only CMMC-specific fine-tuned LLM suite in the open-source ecosystem. Four models (7B–72B) trained for $77 total compute, deployed fully air-gapped via Ollama. 708 tests across three tiers — including 140 blind holdout scenarios. 27 CMMC controls across 5 families (AC, AU, IA, SC, SI) plus 3 DFARS clauses.

| Model | Size | HuggingFace |
|-------|------|-------------|
| cmmc-expert-7b | 5.1 GB | [Nathan-Maine/cmmc-expert-7b](https://huggingface.co/Nathan-Maine/cmmc-expert-7b) |
| cmmc-expert-14b | ~10 GB | [Nathan-Maine/cmmc-expert-14b](https://huggingface.co/Nathan-Maine/cmmc-expert-14b) |
| cmmc-expert-32b | 18.5 GB | [Nathan-Maine/cmmc-expert-32b](https://huggingface.co/Nathan-Maine/cmmc-expert-32b) |
| cmmc-expert-72b | 44.2 GB | [Nathan-Maine/cmmc-expert-72b](https://huggingface.co/Nathan-Maine/cmmc-expert-72b) |

| Repository | What It Does |
|---|---|
| [**cmmc-compliance-ai-model**](https://github.com/NathanMaine/cmmc-compliance-ai-model) | 4 fine-tuned LLMs for CMMC 2.0, NIST 800-171, HIPAA — air-gapped, zero-cloud deployment |
| [**governed-llm-gateway**](https://github.com/NathanMaine/governed-llm-gateway) | Policy-as-code LLM gateway with SHA-256 tamper-evident audit trails — 103 tests |
| [**garak-compliance-probes**](https://github.com/NathanMaine/garak-compliance-probes) | 4 probes + 6 detectors for NVIDIA's garak vulnerability scanner — [PR #1619](https://github.com/NVIDIA/garak/pull/1619) |
| [**governance-graph-compiler**](https://github.com/NathanMaine/governance-graph-compiler) | Converts governance policy Markdown into enforceable directed acyclic graphs |

---

## 🧠 Expert Knowledge Systems

Building AI-queryable knowledge bases from expert content — video, audio, blogs, documentation. Production system running 130,000+ searchable chunks across 36+ domain experts with GPU-accelerated ingestion and cross-encoder reranking. Accessible from any AI tool via MCP.

| Repository | What It Does |
|---|---|
| [**rah-qdrant-integration**](https://github.com/NathanMaine/rah-qdrant-integration) | Qdrant vector search integration for knowledge graphs — Docker, CLI tools, cross-platform (macOS/Linux/Windows) |

---

## 🤖 Agentic AI Systems

Purpose-built components for agent memory, recovery, planning, and coordination. Deterministic and auditable.

| Repository | What It Does |
|---|---|
| [**agentic-ai-portfolio**](https://github.com/NathanMaine/agentic-ai-portfolio) | Umbrella repo: orchestration + documentation for the agent suite |
| [**agentic-memory-graph-engine**](https://github.com/NathanMaine/agentic-memory-graph-engine) | Graph-based memory with explain() reasoning traces |
| [**self-healing-agentic-workflows**](https://github.com/NathanMaine/self-healing-agentic-workflows) | Retry logic, fallback chains, circuit breakers for agent tasks |
| [**temporal-executive-agent**](https://github.com/NathanMaine/temporal-executive-agent) | Dependency-ordered planning and execution with state tracking |
| [**multi-agent-fairness-governor**](https://github.com/NathanMaine/multi-agent-fairness-governor) | Weighted round-robin allocation with skew-ratio detection |
| [**agentic-workflow-simplifier**](https://github.com/NathanMaine/agentic-workflow-simplifier) | Lightweight Python library for defining multi-agent workflows as directed graphs |
| [**mcp-conversational-data-agent**](https://github.com/NathanMaine/mcp-conversational-data-agent) | MCP server exposing database/CRM/ticket tools to LLMs |
| [**agentic-evaluation-sandbox**](https://github.com/NathanMaine/agentic-evaluation-sandbox) | Doer/Judge holdout scenario evaluation harness |
| [**blind-scenario-testing**](https://github.com/NathanMaine/blind-scenario-testing) | Framework for blind behavioral testing of live API systems — 151 tests |
| [**semantic-test-coverage-agent**](https://github.com/NathanMaine/semantic-test-coverage-agent) | AST-based source/test scanner that finds untested code paths |

---

## 🎙️ Real-Time AI & Meeting Intelligence

| Repository | What It Does |
|---|---|
| [**Project-Aurora-Echo**](https://github.com/NathanMaine/Project-Aurora-Echo) | AI meeting copilot — real-time transcription, speaker diarization, structured summaries. [v2.0](https://github.com/NathanMaine/Project-Aurora-Echo-v2.0): NVIDIA GPU acceleration |
| [**realtime-ai-assistant**](https://github.com/NathanMaine/realtime-ai-assistant) | Four iterations: [vanilla](https://github.com/NathanMaine/realtime-ai-assistant) → [v2](https://github.com/NathanMaine/realtime-ai-assistant002) → [FastAPI](https://github.com/NathanMaine/realtime-ai-assistant003-fast-api) → [Streamlit](https://github.com/NathanMaine/realtime-ai-assistant004-stream-lit) |

---

## 🎯 AI Model Serving

| Repository | What It Does |
|---|---|
| [**el-barto-serve**](https://github.com/NathanMaine/el-barto-serve) | OpenAI-compatible server for ByteDance's mask-diffusion code LLM. Auto-patches Flash Attention for Blackwell GPUs. [Landing page](https://nathanmaine.github.io/el-barto-serve) |

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
| [**bongo_cat_monitor_remix**](https://github.com/NathanMaine/bongo_cat_monitor_remix) | ESP32 animated desk buddy — CPU/RAM/WPM monitor with meme triggers |
| [**Github-Avatar-Rotator**](https://github.com/NathanMaine/Github-Avatar-Rotator) | Automated GitHub avatar rotation via API |

</details>

---

Plus private repositories covering compliance training data pipelines, podcast production platform, and infrastructure automation.

**MIT** AI/ML Certificate · **Salesforce:** Data Cloud Consultant · Administrator · AI Associate · **Scrum:** CSM · **NVIDIA Inception** Member

nmaine@gmail.com · [LinkedIn](https://www.linkedin.com/in/nathanmaine) · [nathanmaine.com](https://nathanmaine.com) · [memoriant.ai](https://memoriant.ai) · [HuggingFace](https://huggingface.co/Nathan-Maine)
