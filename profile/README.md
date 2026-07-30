<div align="center">

# Nathan Maine

### I run enterprise AI programs. And I build the systems myself.

**Senior Technical Program Manager | AI Platform and Infrastructure | Enterprise Delivery**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nathanmaine)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat&logo=huggingface&logoColor=black)](https://huggingface.co/Nathan-Maine)
[![NVIDIA Inception](https://img.shields.io/badge/NVIDIA_Inception-76B900?style=flat&logo=nvidia&logoColor=white)](#)
[![Email](https://img.shields.io/badge/Email-nmaine%40gmail.com-red?style=flat&logo=gmail&logoColor=white)](mailto:nmaine@gmail.com)

**$20M+ program portfolio** · **700,000-user identity platform** · **89M records unified into 45.9M profiles** · **13 fine-tuned LLMs** · **code merged into NVIDIA garak** · **a DGX Spark running 24/7 on my desk**

</div>

> *"Mid-competition, a participant named Nathan Maine built a 30-second GPU benchmark script for Runpod pods and shared it with other competitors. Nobody asked him to. That kind of tooling gets built when the infrastructure is part of your workflow, not just a resource you're renting."*
>
> — **RunPod**, [*OpenAI Parameter Golf: what 1,100 researchers built in six weeks*](https://www.runpod.io/blog/openai-parameter-golf-runpod-challenge)

---

## The Combination

Most program managers manage. Most builders build. The rare thing is one person who has done both at scale, because that person can translate between the boardroom and the terminal without losing anything in either direction.

| I deliver programs | I build systems | I prove it |
|---|---|---|
| $20M+ concurrent multi-cloud portfolio, one of two program leaders across eight workstreams | 13 fine-tuned LLMs across 8 architectures (7B-72B), served fully air-gapped | Adversarial prompts merged into [NVIDIA garak](https://github.com/NVIDIA/garak/pull/1660), shipped in v0.15.0 |
| 700,000-user Okta identity program, Day 1 merger cutover 100% on time, zero unplanned outages | An 80B sparse MoE served on one DGX Spark at ~70 tok/s with tool-calling | CUDA fix merged into an 854-star llama.cpp fork ([TurboQuant #84](https://github.com/TheTom/llama-cpp-turboquant/pull/84)) |
| 89M records across 28 source systems resolved into 45.9M unified profiles at 95.48% match | Policy-as-code LLM gateway with tamper-evident audit trails, 103 tests | Named in RunPod's blog for tooling nobody asked me to build |
| Two 5/5 executive CSAT scores from Fortune 500 clients | Evaluation harness that produced a documented negative result, and shipped it anyway | Benchmarks published to r/LocalLLaMA, Hacker News, and NVIDIA forums |

**Every claim on this page links to something you can check.** The ones that don't fit in a link, ask me about.

---

# Flagship Work

## 1 · Serving an 80B Model on One DGX Spark

**A complete, reproducible recipe for serving Qwen3-Coder-Next (80B total / 3B active sparse MoE) as an OpenAI-compatible API on a single DGX Spark, with working tool-calling and real multi-user concurrency.**

The decisive details were scattered across NVIDIA forum threads, GitHub issues in three repos, model cards, and a community Docker project: which checkpoint actually performs (a native int4 AutoRound quant, not a GGUF), the one environment variable the int4 kernels need, why driver 590+ matters (CUDA graphs on GB10: 2.8x single-stream speed), and the Secure Boot DKMS trap that hangs installs. This repo puts the working configuration, the reasoning behind every setting, and an honest account of every dead end in one place.

| What you get | Number | What it means |
|---|---|---|
| Solo user | ~70 tok/s | The number that matters if it's just you |
| Each of 16 concurrent users | ~22 tok/s | What a person actually experiences under full load |
| Whole-box aggregate | ~350 tok/s | A capacity measure, not a speed; the repo explains why |

Confirmed by vLLM's server-side accounting, not client timers. 131K context. The repo documents which claims from its own first draft were wrong and got fixed before publishing.

[![GitHub](https://img.shields.io/badge/GitHub-NVIDIA--DGX--Spark--with--vLLM-76B900?style=for-the-badge&logo=github)](https://github.com/NathanMaine/NVIDIA-DGX-Spark-with-vLLM)

## 2 · NeuralForge

![NeuralForge](https://github.com/user-attachments/assets/68ead074-d399-4b18-9775-1c4d7ff41d29)

**GPU-native knowledge intelligence platform built on 6 NVIDIA technologies.** Your experts. Your GPU. Your data never leaves.

Ingest domain expertise at scale, build GPU-accelerated relationship graphs with RAPIDS cuGraph, and serve answers through any OpenAI-compatible tool. Built on NIM, TensorRT-LLM, Triton, NeMo Guardrails, cuGraph, and CUDA.

*Active development / reference architecture: built and tested (1,006 passing tests), not yet a turnkey end-to-end deploy. See the repo Status section.*

[![GitHub](https://img.shields.io/badge/GitHub-neuralforge-76B900?style=for-the-badge&logo=github)](https://github.com/NathanMaine/neuralforge)
[![Tests](https://img.shields.io/badge/Tests-1006_passing-brightgreen?style=for-the-badge)](https://github.com/NathanMaine/neuralforge)
[![License](https://img.shields.io/badge/License-Apache_2.0-blue?style=for-the-badge)](https://github.com/NathanMaine/neuralforge/blob/main/LICENSE)

## 3 · CMMC Compliance AI

**13 fine-tuned LLMs across 8 architectures (7B-72B) for cybersecurity compliance: CMMC 2.0, NIST 800-171, HIPAA. Served fully air-gapped, because the organizations that need compliance AI most are the ones that cannot send data to a cloud API.**

Flagship: Gemma 4 31B (eval loss 0.4517). QLoRA/DoRA fine-tuning, GGUF export, Ollama deployment. Training data: [18,747 curated compliance examples](https://huggingface.co/datasets/Nathan-Maine/cmmc-training-data-2026-q2) across 11 regulatory frameworks, rebuilt from 67K raw examples with 73% noise removed.

[![GitHub](https://img.shields.io/badge/GitHub-cmmc--compliance--ai--model-blue?style=for-the-badge&logo=github)](https://github.com/NathanMaine/cmmc-compliance-ai-model)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-Nathan--Maine-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/Nathan-Maine)

## 4 · Promptx

**Turns a vague request into an explicit work order, so local coding models execute instead of guessing.**

Born from a real failure: a local 80B model was asked to "build out the gtm adapters package." It wrote an `__init__.py` importing three sibling modules that did not exist, saw an ImportError naming `__init__.py`, and rewrote `__init__.py`. Ten times. The model was not broken; it was fixing the file the error named instead of creating the files that were missing. The lesson generalizes: **local models follow explicit instructions well and infer badly. Ambiguity is what makes them loop.**

So Promptx splits the job. A cheap, fast cloud model (~$0.10 per million tokens) converts intent into a precise, numbered spec with real file paths, because it reads your actual file tree instead of inventing plausible ones. Your local model, excellent at execution and weak at inference, runs the spec. Fraction of a cent per request. Zero dependencies: Python 3.9+ standard library only, on purpose. `--snap` records a baseline before the agent works; `--check` verifies what it actually did.

[![GitHub](https://img.shields.io/badge/GitHub-Promptx-blue?style=for-the-badge&logo=github)](https://github.com/NathanMaine/Promptx)

---

# Open Source: Merged and Credited

| Contribution | Status | Proof |
|---|---|---|
| Homoglyph obfuscation prompts, NVIDIA garak smuggling probe | **Merged, shipped in v0.15.0** | [PR #1660](https://github.com/NVIDIA/garak/pull/1660) |
| CUDA flash-attention dispatch fix, TurboQuant (854-star llama.cpp fork) | **Merged**, validated on RTX 4090 and DGX Spark GB10 | [PR #84](https://github.com/TheTom/llama-cpp-turboquant/pull/84) |
| PyTorch version verification, runpod/containers | Closed in favor of a hardened version; **maintainer preserved my commit with credit** | [PR #115](https://github.com/runpod/containers/pull/115), [issue #114](https://github.com/runpod/containers/issues/114) |
| Fabricated regulatory citation probe suite, NVIDIA garak | Under review | [PR #1658](https://github.com/NVIDIA/garak/pull/1658), [Discussion #1659](https://github.com/NVIDIA/garak/discussions/1659) |

## OpenAI Parameter Golf

*Competition work is under my dentity007 handle (which displays as Nathan Maine).*

Training the best language model in 16MB on 8xH100s. Implemented all 7 of OpenAI's explicitly requested research directions, with 8 complete training scripts (11,810 lines of novel research code) and 95+ GPU experiments across RTX 5090, H100, and H200 SXM pods. Novel techniques developed beyond the requests: Adaptive Density Training, Echo Training, Gradient Quilting.

**Companion dashboard:** [parameter-golf-experiment-lab](https://github.com/NathanMaine/parameter-golf-experiment-lab), a [live interactive visualization](https://nathanmaine.github.io/parameter-golf-experiment-lab/) of 793+ scored community submissions with TTT-legality filtering, my 95+ experiment log, technique matrix, and cost analysis.

<details>
<summary><b>Full submission tables (record, neural track, and all 7 research architectures)</b></summary>

**Record Submissions (3-seed verified):**

| PR | Architecture | BPB |
|----|-------------|-----|
| [#968](https://github.com/openai/parameter-golf/pull/968) | Order-20 Dirichlet Posterior + Per-Order OBCL + Phrase Cache | **0.1154** |
| [#948](https://github.com/openai/parameter-golf/pull/948) | Two-Level Dirichlet Posterior + Phrase Cache | **0.1156** |
| [#1127](https://github.com/openai/parameter-golf/pull/1127) | 11L XSA-all + EMA + LoRA TTT + Partial RoPE + dim480 | **1.1311** |

**Neural Track (progressive improvement):**

| PR | Architecture | BPB | Seeds |
|----|-------------|-----|-------|
| [#406](https://github.com/openai/parameter-golf/pull/406) | 11L XSA4 + EMA + Self-Distillation TTT | 1.1287 | 3 |
| [#385](https://github.com/openai/parameter-golf/pull/385) | 11L Int6 QAT + SmearGate + SWA(0.4) + WD=0.04 | 1.1488 | 3 |
| [#273](https://github.com/openai/parameter-golf/pull/273) | 10L Int6 QAT + SmearGate + SWA | 1.1575 | 1 |

**Research Submissions (all 7 OpenAI-requested architectures):**

| PR | Architecture | BPB |
|----|-------------|-----|
| [#1192](https://github.com/openai/parameter-golf/pull/1192) | Fused Triton Megakernels (RMSNorm + LeakyReLU) | 1.356 |
| [#1191](https://github.com/openai/parameter-golf/pull/1191) | H-Net Dynamic Chunking (learned tokenization) | 1.359 |
| [#1193](https://github.com/openai/parameter-golf/pull/1193) | Universal Transformer + Adaptive Density | 1.439 |
| [#1195](https://github.com/openai/parameter-golf/pull/1195) | Learning Adapters on Random Linear Maps | 2.202 |
| [#1196](https://github.com/openai/parameter-golf/pull/1196) | LLM-JEPA (Joint Embedding Prediction) | 2.202 |
| [#1197](https://github.com/openai/parameter-golf/pull/1197) | Mamba-Inspired SSM Hybrid (3:1 SSM:Attention) | 3.317 |
| [#1194](https://github.com/openai/parameter-golf/pull/1194) | Text Diffusion (MDLM, masked discrete diffusion) | 3.380 |

**Infrastructure built:** 486K+ chunk expert knowledge base from 80+ AI/ML experts. Competitive intelligence pipeline analyzing 1,084 competitor PRs. Multi-pod experiment orchestration. Full Hessian GPTQ validation on Hopper (H200 SXM).

</details>

---

# The Catalog

<details>
<summary><b>AI/ML Infrastructure and Platform Engineering</b> — training pipelines, inference serving, benchmarks</summary>

| Project | What It Does | Stack |
| --- | --- | --- |
| [**NVIDIA-DGX-Spark-with-vLLM**](https://github.com/NathanMaine/NVIDIA-DGX-Spark-with-vLLM) | End-to-end serving recipe for an 80B sparse MoE on one Spark, throughput stated honestly and confirmed server-side | vLLM, CUDA, aarch64 |
| [**cmmc-compliance-ai-model**](https://github.com/NathanMaine/cmmc-compliance-ai-model) | 13 fine-tuned LLMs across 8 architectures for regulated industries, air-gapped | PyTorch, Unsloth, Ollama |
| [**dgx-spark-kv-cache-benchmark**](https://huggingface.co/datasets/Nathan-Maine/dgx-spark-kv-cache-benchmark) | KV-cache quantization benchmarks on GB10 (q4/q8/f16 at long context). Published to r/LocalLLaMA, HN, NVIDIA Forums | llama.cpp, CUDA 13.0 |
| [**nv-ingest-document-pipeline**](https://github.com/NathanMaine/nv-ingest-document-pipeline) | GPU-accelerated PDF extraction to chat-format JSONL training data. 61 tests, 95% coverage, mypy strict | nv-ingest, Docker |
| [**runpod-gpu-benchmark**](https://github.com/NathanMaine/runpod-gpu-benchmark) | The 30-second GPU sanity check RunPod wrote about | Shell, CUDA |
| [**el-barto-serve**](https://github.com/NathanMaine/el-barto-serve) | OpenAI-compatible inference server, auto-patches Flash Attention for Blackwell | Python, PyTorch |
| [**memoriant-ops-bot**](https://github.com/NathanMaine/memoriant-ops-bot) | Multi-provider AI agent orchestration via Telegram/Matrix | Python, WebSocket |

</details>

<details>
<summary><b>Agentic AI and Evaluation Systems</b> — evaluation, recovery, orchestration</summary>

| Project | What It Does | Link |
| --- | --- | --- |
| **Evaluation Sandbox** | Doer/Judge/Adversary/Observer holdout scenario evaluation | [Repo](https://github.com/NathanMaine/agentic-evaluation-sandbox) |
| **Blind Scenario Testing** | Black-box behavioral testing of live API systems, 151 tests | [Repo](https://github.com/NathanMaine/blind-scenario-testing) |
| **Promptx** | Vague request to explicit work order for local coding agents | [Repo](https://github.com/NathanMaine/Promptx) |
| **Self-Healing Workflows** | Retry logic, fallback chains, circuit breakers for agent tasks | [Repo](https://github.com/NathanMaine/self-healing-agentic-workflows) |
| **Temporal Executive Agent** | Dependency-ordered planning and execution with state tracking | [Repo](https://github.com/NathanMaine/temporal-executive-agent) |
| **MCP Data Agent** | MCP server exposing CRM/ticket/database tools to LLMs | [Repo](https://github.com/NathanMaine/mcp-conversational-data-agent) |
| **Fairness Governor** | Weighted round-robin allocation with skew-ratio detection | [Repo](https://github.com/NathanMaine/multi-agent-fairness-governor) |

Full suite: [agentic-ai-portfolio](https://github.com/NathanMaine/agentic-ai-portfolio)

</details>

<details>
<summary><b>Compliance and Security Automation</b> — governance for regulated environments</summary>

| Project | What It Does | Link |
| --- | --- | --- |
| **garak Compliance Probes** | LLM vulnerability probes for NVIDIA garak (see Merged and Credited above) | [Repo](https://github.com/NathanMaine/garak-compliance-probes) |
| **Governed LLM Gateway** | Policy-as-code gateway: tamper-evident audit trails, rate limiting, cost telemetry. 103 tests | [Repo](https://github.com/NathanMaine/governed-llm-gateway) |
| **Governed Voice Agent** | Policy-as-code governance, tamper-evident audit, and per-call cost attribution for LiveKit voice agents, with Doer/Judge governance evals | [Repo](https://github.com/NathanMaine/governed-voice-agent) |
| **Governance Graph Compiler** | Compiles policy Markdown into DAGs for deterministic audit evaluation | [Repo](https://github.com/NathanMaine/governance-graph-compiler) |
| **Patent Platform** | Full patent pipeline: search, analyze, draft, review, file. 706+ tests | [Repo](https://github.com/NathanMaine/memoriant-patent-platform) |

</details>

<details>
<summary><b>Speech AI, Tutorials, and the Plugin Marketplace</b></summary>

**Speech:** [speech-systems](https://github.com/NathanMaine/speech-systems), the hub for a 6-version AI meeting copilot progression (Aurora Echo), a batch ASR pipeline (NVIDIA Parakeet on DGX Spark), and TTS orchestration.

**Tutorials, teaching ML by building from scratch:**

| Tutorial | What You Build | Link |
| --- | --- | --- |
| **smallest-ai-tutorial** | 4 neural networks from scratch in pure Python (MLP, LSTM, Transformer, BitNet). 273 tests | [Repo](https://github.com/NathanMaine/smallest-ai-tutorial) |
| **smallest-ai-built-from-the-ground-up** | Full project: all 4 architectures, C export for ESP32, ARM QEMU verification | [Repo](https://github.com/NathanMaine/smallest-ai-built-from-the-ground-up) |

**Claude Code Plugin Marketplace:** [14 published plugins](https://github.com/NathanMaine/memoriant-marketplace) for AI-powered development workflows: architecture review, load testing, documentation drift detection, governance compilation, test coverage analysis, eval sandboxes, and more.

</details>

---

# Enterprise Delivery Record

Ten years of technical program management. The systems above get built at night; these ship during the day.

| Domain | Proof Points |
| --- | --- |
| **Platform Scale** | $20M+ portfolios, 700K-user identity systems, multi-cloud (Sales/Service/Data Cloud) |
| **Cross-Team Execution** | Two 5/5 executive CSAT scores from Fortune 500 clients; SSO onboarding cut from 6 weeks to 2 (67%) |
| **Security and Identity** | ~200-application SSO program (Okta/SAML/OIDC) across federated business divisions |
| **Data Platforms** | 89M records across 28 source systems resolved into 45.9M unified profiles; match quality 87% to 95.48% |
| **Compliance** | SOC 2, PCI DSS, HIPAA, FERPA, and NIST 800-171 delivery across regulated engineering environments |
| **Regulated Environments** | Air-gapped AI deployment, CUI-handling systems, DFARS-adjacent compliance tooling |

## The Lab

- **NVIDIA DGX Spark** (GB10, 128GB unified memory) running daily: Qwen3-Coder-Next at ~70 tok/s solo via vLLM, Gemma 4 26B A4B at 43 tok/s
- **486K+ knowledge chunks** from 80+ AI/ML experts
- 10G backbone connecting DGX Spark, NAS (3.6TB models), and workstations
- For heavy training: 8xH100 SXM on RunPod, torchrun DDP, torch.compile, FA3

---

<div align="center">

**MIT Professional Education:** No Code AI and Machine Learning | **Salesforce:** five certifications plus Financial Services Cloud Accredited Professional | **Scrum:** CSM | **AI Security and Governance** (Securiti) | **NVIDIA Inception** Member

Currently: AI Solutions Advisor at Glocal Advantage.
If you are building something where enterprise delivery meets AI, my inbox is open.

📧 **nmaine@gmail.com** · [LinkedIn](https://www.linkedin.com/in/nathanmaine) · [HuggingFace](https://huggingface.co/Nathan-Maine)

</div>
