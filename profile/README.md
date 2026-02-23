# Nathan Maine

**Senior Technical Program Manager | AI Systems Builder | 12+ Years Enterprise Delivery**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nathanmaine)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat&logo=huggingface&logoColor=black)](https://huggingface.co/Nathan-Maine)
[![Website](https://img.shields.io/badge/Website-000000?style=flat&logo=safari&logoColor=white)](https://nathanmaine.com)
[![Podcast](https://img.shields.io/badge/Podcast-8B5CF6?style=flat&logo=spotify&logoColor=white)](https://podcast.nathanmaine.com)

I build the AI systems I've spent a career learning to manage — compliance LLMs, governed inference gateways, evaluation harnesses for autonomous agents, and patent-pending token governance infrastructure. 12 years enterprise delivery across identity platforms (700K users), data unification (89M records, 95.48% match rates), and $20M+ multi-cloud programs.

---

## CMMC Compliance AI Platform (v1.5.1)

The only CMMC-specific fine-tuned LLM suite in the open-source ecosystem. Four models (7B–72B) trained for $77 total compute, deployed fully air-gapped via Ollama. 708 tests across three tiers — including 140 blind holdout scenarios that caught 3 real security bugs the 568 internal tests missed. 27 CMMC controls across 5 families (AC, AU, IA, SC, SI) plus 3 DFARS clauses.

| Model | Size | HuggingFace |
|-------|------|-------------|
| cmmc-expert-7b | 5.1 GB | [Nathan-Maine/cmmc-expert-7b](https://huggingface.co/Nathan-Maine/cmmc-expert-7b) |
| cmmc-expert-14b | ~10 GB | [Nathan-Maine/cmmc-expert-14b](https://huggingface.co/Nathan-Maine/cmmc-expert-14b) |
| cmmc-expert-32b | 18.5 GB | [Nathan-Maine/cmmc-expert-32b](https://huggingface.co/Nathan-Maine/cmmc-expert-32b) |
| cmmc-expert-72b | 44.2 GB | [Nathan-Maine/cmmc-expert-72b](https://huggingface.co/Nathan-Maine/cmmc-expert-72b) |

| Repository | Problem It Solves | How It Works |
|---|---|---|
| [**governed-llm-gateway**](https://github.com/NathanMaine/governed-llm-gateway) | Commercial AI gateways log to editable databases — useless for compliance audits | Every AI request passes through an 11-step pipeline that logs who asked what, blocks sensitive data, and chains each entry to the previous one using SHA-256 hashes — any tampering breaks the chain |
| [**cmmc-compliance-ai-model**](https://github.com/NathanMaine/cmmc-compliance-ai-model) | CMMC compliance consultants cost $125K–$250K and no open-source AI alternative exists | Four AI models fine-tuned on government compliance documents, sized from fast lookups (7B) to deep multi-framework analysis (72B), running entirely on local hardware with zero cloud dependency |
| [**garak-compliance-probes**](https://github.com/NathanMaine/garak-compliance-probes) | Standard AI vulnerability scanners don't test whether models leak regulated data like CUI, HIPAA, or DFARS content | Four custom probes and six detectors for NVIDIA's garak scanner that specifically try to trick compliance models into revealing controlled information. [PR #1619](https://github.com/NVIDIA/garak/pull/1619) — 20 files, 1,599 lines. [Dev fork](https://github.com/NathanMaine/garak) |
| [**governance-graph-compiler**](https://github.com/NathanMaine/governance-graph-compiler) | Compliance policies written in documents are hard to trace and enforce with software | Reads policy Markdown files and converts them into a connected graph where each requirement links to its evidence artifacts and enforcement points |

---

## AI Agent Evaluation & Dark Factory Testing

140 black-box behavioral scenarios in a physically separate holdout repository — the AI that builds the platform never sees the tests. An agent cannot game what it cannot see. The first sweep caught 3 real security bugs that passed all 568 internal tests: broken MFA setup (High), missing X-Content-Type-Options header (Medium), and missing X-Frame-Options header (Medium). This architecture independently converged with [StrongDM's Software Factory](https://factory.strongdm.ai) pattern (published February 2026). The [Agentic Evaluation Sandbox](https://github.com/NathanMaine/agentic-evaluation-sandbox) was created **December 2025**, predating their publication.

| Repository | Problem It Solves | How It Works |
|---|---|---|
| [**cmmc-scenario-holdout**](https://github.com/NathanMaine/cmmc-scenario-holdout) | 568 internal tests all passed but 3 real security bugs shipped — visible tests get gamed by AI agents | 140 black-box HTTP scenarios in a separate repo the AI never sees. Docker digital twin with mock Ollama (no GPU). Covers auth, RBAC, PII/CUI blocking, prompt injection, audit integrity, security headers, and 8 CMMC policy rules. First sweep caught 3 bugs — all fixed in v1.5.1 |
| [**agentic-evaluation-sandbox**](https://github.com/NathanMaine/agentic-evaluation-sandbox) | AI agents can learn to game their own tests when the tests live inside the codebase | The original Dark Factory framework (December 2025). Defines four evaluation roles — Doer, Judge, Adversary, Observer — with holdout scenarios and probabilistic satisfaction scoring instead of simple pass/fail |
| [**agentic-ai-portfolio**](https://github.com/NathanMaine/agentic-ai-portfolio) | Five independent agent repos need a single entry point for orchestration and documentation | Umbrella repository tying together AES, GGC, AMG, SHAW, and TEA with shared configuration and docs |
| [**voice-robustness-testing-agent**](https://github.com/NathanMaine/voice-robustness-testing-agent) | Voice assistants and NLU classifiers break under noisy or unusual input — failures need to be found before users find them | Injects noise, varied phrasing, and edge cases into voice endpoints, classifies each response into three outcome states, and generates a robustness report with evidence |
| [**agent-perf-test-generator**](https://github.com/NathanMaine/agent-perf-test-generator) | Writing load test plans for steady traffic, burst traffic, and endurance runs is repetitive and error-prone | Takes a service profile and SLO targets as input, then generates ready-to-run test configurations with pass/fail thresholds derived directly from the SLOs |
| [**semantic-test-coverage-agent**](https://github.com/NathanMaine/semantic-test-coverage-agent) | Line coverage numbers don't tell you whether every function's actual behavior is tested | Walks the code's syntax tree to find every function, matches each one against existing test files, and generates skeleton tests for anything that's untested |

---

## Agent Infrastructure

Purpose-built components for agent memory, recovery, planning, and coordination. Deterministic and auditable — identical inputs always produce identical outputs.

| Repository | Problem It Solves | How It Works |
|---|---|---|
| [**agentic-memory-graph-engine**](https://github.com/NathanMaine/agentic-memory-graph-engine) | AI agents forget what happened in previous tasks — they have no persistent, queryable memory | Stores facts and relationships in a knowledge graph, retrieves relevant memories using similarity search, and can explain why it recalled something by tracing the graph path |
| [**self-healing-agentic-workflows**](https://github.com/NathanMaine/self-healing-agentic-workflows) | When an AI agent fails mid-task, most systems just crash instead of recovering | Wraps agent tasks in retry logic with exponential backoff, fallback chains (try Plan B if Plan A fails), and circuit breakers that stop calling a broken service |
| [**temporal-executive-agent**](https://github.com/NathanMaine/temporal-executive-agent) | Complex tasks have dependencies — step A must finish before step B can start — and agents often ignore this | Builds a dependency graph of subtasks, resolves ordering constraints, and executes them in valid sequence while tracking state at each step |
| [**multi-agent-fairness-governor**](https://github.com/NathanMaine/multi-agent-fairness-governor) | When multiple agents compete for tasks, some get overloaded while others sit idle | Coordinates agents using weighted round-robin allocation with capacity constraints and a skew-ratio metric that detects and corrects workload imbalance |
| [**agentic-workflow-simplifier**](https://github.com/NathanMaine/agentic-workflow-simplifier) | Defining multi-agent workflows usually requires heavy frameworks with steep learning curves | Lightweight Python library that lets you define workflows as directed graphs with automatic dependency resolution and feedback loops |
| [**mcp-conversational-data-agent**](https://github.com/NathanMaine/mcp-conversational-data-agent) | LLMs can't natively query databases or CRM systems during a conversation | Model Context Protocol server that exposes database, CRM, and ticket system tools so an LLM can query structured data through natural language |

---

<details>
<summary><strong>Developer Experience & Operations</strong> (8 projects)</summary>

| Repository | Problem It Solves | How It Works |
|---|---|---|
| [**architectural-design-review-agent**](https://github.com/NathanMaine/architectural-design-review-agent) | Architecture reviews are inconsistent — different reviewers check different things | Accepts YAML architecture briefs, runs them through an LLM, and generates structured reviews with risk assessments, open questions, and checklists. Includes stub mode for testing without an LLM |
| [**living-docforce-agent**](https://github.com/NathanMaine/living-docforce-agent) | Documentation goes stale the moment code changes — nobody notices until it's already wrong | Compares code and config files against their corresponding docs, labels each gap by severity, and logs evidence of every drift it finds |
| [**meeting-memory-companion**](https://github.com/NathanMaine/meeting-memory-companion) | Meeting notes are unstructured text — you can't search "who owns action item X?" without reading everything | Extracts attendees, decisions, and action items from raw meeting notes using 6-category classification into a structured, queryable record |
| [**devex-metrics-dashboard**](https://github.com/NathanMaine/devex-metrics-dashboard) | Teams can't see their developer experience health at a glance — they rely on gut feel | Ingests delivery signals (build times, PR cycle time, incident counts) and computes 7 DORA-aligned health indicators with a compact status snapshot |
| [**devex-env-bootstrap-agent**](https://github.com/NathanMaine/devex-env-bootstrap-agent) | New developers waste days setting up their local environment because setup docs are stale or missing | Scans the project folder, detects languages and dependencies, and generates a bootstrap script plus onboarding checklist automatically |
| [**ai-ops-kpi-pipeline**](https://github.com/NathanMaine/ai-ops-kpi-pipeline) | AI operations metrics are scattered across tools with no unified view | ETL pipeline that ingests KPI snapshots from multiple sources, aggregates them using suffix-based heuristics, and produces a single evidence-backed report |
| [**ai-deployment-experience-bot**](https://github.com/NathanMaine/ai-deployment-experience-bot) | Developers switch between Slack and deployment dashboards to trigger deploys and check status | Slack bot that lets developers trigger deployments, rollbacks, and status checks via simple chat commands without leaving the conversation |
| [**agent-zero-dashboard**](https://github.com/NathanMaine/agent-zero-dashboard) | Agent Zero's autonomous tasks run in the background with no visibility into what it's doing or why | Real-time monitoring dashboard that visualizes Agent Zero's current state, task queue, and execution history |

</details>

<details>
<summary><strong>Real-Time AI & Meeting Intelligence</strong> (6 projects)</summary>

| Repository | Problem It Solves | How It Works |
|---|---|---|
| [**Project-Aurora-Echo**](https://github.com/NathanMaine/Project-Aurora-Echo) | Meetings produce hours of audio — decisions and action items get lost because nobody re-listens | Captures audio in real time, transcribes with faster-whisper, identifies who said what via speaker diarization, and generates structured summaries through an LLM. [v2.0](https://github.com/NathanMaine/Project-Aurora-Echo-v2.0) adds NVIDIA GPU acceleration |
| [**realtime-ai-assistant**](https://github.com/NathanMaine/realtime-ai-assistant) | Same core problem — exploring different architectures for live meeting transcription and summarization | Evolved through four iterations: [vanilla Python](https://github.com/NathanMaine/realtime-ai-assistant) → [improved pipeline](https://github.com/NathanMaine/realtime-ai-assistant002) → [FastAPI + WebSocket](https://github.com/NathanMaine/realtime-ai-assistant003-fast-api) → [Streamlit UI](https://github.com/NathanMaine/realtime-ai-assistant004-stream-lit), each using xAI Grok for live summarization |

</details>

<details>
<summary><strong>Salesforce / Agentforce</strong> (3 projects)</summary>

| Repository | Problem It Solves | How It Works |
|---|---|---|
| [**Agentforce-Data-Aware-Agent**](https://github.com/NathanMaine/Agentforce-Data-Aware-Agent) | Salesforce AI agents can access org data without respecting field-level security or sharing rules — a compliance risk | Auto-discovers the org schema (objects, fields, relationships), enforces FLS and sharing rules, then runs safe actions (SOQL, Flow, Apex) within those boundaries |
| [**Agentforce-Dynamic-Action**](https://github.com/NathanMaine/Agentforce-Dynamic-Action) | Every new Salesforce agent capability requires manually writing Apex code | Takes a natural-language goal description and generates working Apex code on the fly to execute it |
| [**Agentforce-Dynamic-Action-Invocable**](https://github.com/NathanMaine/Agentforce-Dynamic-Action-Invocable) | The Dynamic Action pattern needs to work inside Salesforce Flows, Einstein Copilot, and REST — not just standalone | Invocable wrapper that exposes the dynamic action generator to Flow, Einstein Copilot, and REST endpoints |

</details>

<details>
<summary><strong>Classical AI & Side Projects</strong> (7 projects)</summary>

| Repository | Problem It Solves | How It Works |
|---|---|---|
| [**LISP-Backward-Chaining-Core-Engine**](https://github.com/NathanMaine/LISP-Backward-Chaining-Core-Engine) | Modern AI is all neural nets — classic rule-based reasoning that can explain its conclusions is underrepresented | Common Lisp expert system that works backward from a goal, checking rules and facts until it can prove or disprove the goal, with certainty scores on every conclusion |
| [**lisp-car-expert-system**](https://github.com/NathanMaine/lisp-car-expert-system) | Demonstrating practical symbolic AI with a real-world application and a complete dev environment | Rule-based car troubleshooting system with a forward chaining inference engine — starts from symptoms and fires rules until it reaches a diagnosis. Includes VS Code + SBCL setup |
| [**Chess-Analyzer-v2**](https://github.com/NathanMaine/Chess-Analyzer-v2) | Analyzing chess games online means switching between multiple tools and sites | React + TypeScript web app that imports Chess.com games, runs in-browser move analysis, and shows performance trends on interactive dashboards |
| [**chess-analyzer**](https://github.com/NathanMaine/chess-analyzer) | Desktop chess analysis with deeper engine integration and multi-provider AI commentary | Cross-platform Python app with Stockfish evaluation, AI-generated move explanations (why was that move bad?), and batch game processing |
| [**Thermomix-Recipe-Genius**](https://github.com/NathanMaine/Thermomix-Recipe-Genius) | Thermomix TM6 recipes need exact weight-based measurements that regular recipes don't provide | React + TypeScript frontend that uses Google Gemini and xAI Grok to generate and convert weight-based Thermomix recipes |
| [**bongo_cat_monitor_remix**](https://github.com/NathanMaine/bongo_cat_monitor_remix) | System monitoring is boring — why not make it fun with an animated desk companion? | ESP32 microcontroller with TFT display: animated Bongo Cat that reacts to CPU usage, RAM, and typing speed, plus meme triggers and Imgflip integration |
| [**Github-Avatar-Rotator**](https://github.com/NathanMaine/Github-Avatar-Rotator) | GitHub avatars get stale — automating rotation keeps the profile fresh | Script that cycles through a set of avatar images using the GitHub API on a schedule |

</details>

---

Plus 8 private repositories covering compliance training data pipelines, SDLC validation, architecture review, and load testing infrastructure.

**MIT** AI/ML Certificate · **Salesforce:** Data Cloud Consultant · Administrator · AI Associate · **Scrum:** CSM

nmaine@gmail.com · [LinkedIn](https://www.linkedin.com/in/nathanmaine) · [nathanmaine.com](https://nathanmaine.com) · [HuggingFace](https://huggingface.co/Nathan-Maine)
