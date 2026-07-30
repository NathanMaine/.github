# Nathan Maine

**Senior Technical Program Manager | AI Platform & Infrastructure | Enterprise Delivery**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nathanmaine)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat&logo=huggingface&logoColor=black)](https://huggingface.co/Nathan-Maine)
[![NVIDIA Inception](https://img.shields.io/badge/NVIDIA_Inception-76B900?style=flat&logo=nvidia&logoColor=white)](#)

Ten years of technical program management across platform engineering, AI/ML infrastructure, and enterprise systems. I drive complex, multi-team technical programs from ambiguity to shipped, measurable outcomes: a $20M+ multi-cloud portfolio, a 700,000-user identity program, and identity resolution of 89M records across 28 source systems into 45.9M unified profiles.

And I build the systems, not just manage them: fine-tuned compliance LLMs, GPU-accelerated inference infrastructure, and agentic evaluation frameworks, deployed on an NVIDIA DGX Spark running 24/7 on my desk.

> *"Mid-competition, a participant named Nathan Maine built a 30-second GPU benchmark script for Runpod pods and shared it with other competitors. Nobody asked him to. That kind of tooling gets built when the infrastructure is part of your workflow, not just a resource you're renting."*
> — RunPod blog, [*OpenAI Parameter Golf: what 1,100 researchers built in six weeks*](https://www.runpod.io/blog/openai-parameter-golf-runpod-challenge) (May 2026). The script: [runpod-gpu-benchmark](https://github.com/NathanMaine/runpod-gpu-benchmark)

---

## NeuralForge

![NeuralForge](https://github.com/user-attachments/assets/68ead074-d399-4b18-9775-1c4d7ff41d29)

**GPU-native knowledge intelligence platform built on 6 NVIDIA technologies.**

Your experts. Your GPU. Your data never leaves.

Ingest domain expertise at scale, build GPU-accelerated relationship graphs with RAPIDS cuGraph, and serve answers through any OpenAI-compatible tool. Built on NIM, TensorRT-LLM, Triton, NeMo Guardrails, cuGraph, and CUDA.

*Active development / reference architecture: built and tested (1,006 passing tests), not yet a turnkey end-to-end deploy. See the repo Status section.*

[![GitHub](https://img.shields.io/badge/GitHub-neuralforge-76B900?style=for-the-badge&logo=github)](https://github.com/NathanMaine/neuralforge)
[![Tests](https://img.shields.io/badge/Tests-1006_passing-brightgreen?style=for-the-badge)](https://github.com/NathanMaine/neuralforge)
[![License](https://img.shields.io/badge/License-Apache_2.0-blue?style=for-the-badge)](https://github.com/NathanMaine/neuralforge/blob/main/LICENSE)

---

## What I Build

| Project | What It Does | Stack |
|---------|-------------|-------|
| [NeuralForge](https://github.com/NathanMaine/neuralforge) | GPU-native knowledge intelligence with temporal knowledge graphs | NIM, TensorRT-LLM, Triton, NeMo Guardrails, cuGraph |
| [DGX Spark + vLLM Serving Recipe](https://github.com/NathanMaine/NVIDIA-DGX-Spark-with-vLLM) | Reproducible recipe serving Qwen3-Coder-Next (80B-A3B MoE) on one DGX Spark: ~70 tok/s solo, 16-user concurrency, 131K context, working tool-calling, with honestly framed throughput numbers | vLLM, GB10, aarch64 |
| [CMMC Compliance AI](https://github.com/NathanMaine/cmmc-compliance-ai-model) | 13 fine-tuned LLMs across 8 architectures (7B to 72B) for cybersecurity compliance (CMMC 2.0, NIST 800-171, HIPAA), served air-gapped | QLoRA, GGUF, Ollama, DGX Spark |
| [Governed LLM Gateway](https://github.com/NathanMaine/governed-llm-gateway) | Policy-as-code gateway with tamper-evident audit trails | FastAPI, SHA-256 hash chains, 103 tests |
| [Promptx](https://github.com/NathanMaine/Promptx) | Turns a vague request into an explicit work order so local coding models execute instead of guessing | Python |
| [Governed Voice Agent](https://github.com/NathanMaine/governed-voice-agent) | Enterprise-readiness layers for LiveKit voice agents: policy-as-code governance, tamper-evident audit trail, per-call cost attribution, Doer/Judge governance evals | LiveKit Agents, Python |
| [Speech-Systems](https://github.com/NathanMaine/speech-systems) | Hub for ASR, TTS, and orchestration speech-AI projects (6-version Aurora Echo progression, ASR pipeline, TTS pipeline) | Parakeet, pyannote, faster-whisper, FastAPI, DGX Spark |
| [Agentic Evaluation Sandbox](https://github.com/NathanMaine/agentic-evaluation-sandbox) | Doer/Judge/Adversary/Observer framework for agent testing | Multi-agent orchestration |
| [garak contribution (merged)](https://github.com/NVIDIA/garak/pull/1660) | Homoglyph obfuscation prompts merged into NVIDIA garak's smuggling probe, shipped in v0.15.0 | Adversarial prompts, Unicode |
| [TurboQuant contribution (merged)](https://github.com/TheTom/llama-cpp-turboquant/pull/84) | CUDA flash-attention dispatch fix, validated cross-architecture on RTX 4090 and DGX Spark GB10 | llama.cpp fork, CUDA |

## Hardware

- **NVIDIA DGX Spark** (GB10, 128GB unified memory) running daily: Qwen3-Coder-Next served at ~70 tok/s solo via vLLM, Gemma 4 26B A4B at 43 tok/s
- **486K+ knowledge chunks** from 80+ AI/ML experts
- 10G office network connecting DGX Spark, NAS, and workstations

---

## AI/ML Infrastructure & Platform Engineering

Production AI systems: model training pipelines, inference serving, evaluation harnesses, and observability.

| Project | What It Does | Stack |
| --- | --- | --- |
| [**cmmc-compliance-ai-model**](https://github.com/NathanMaine/cmmc-compliance-ai-model) | 13 fine-tuned LLMs across 8 architectures (7B-72B) for regulated industries. Flagship: Gemma 4 31B (eval loss 0.4517). QLoRA/DoRA, GGUF, air-gapped Ollama. Eval datasets on [HuggingFace](https://huggingface.co/Nathan-Maine). | PyTorch, Unsloth, CUDA, Ollama |
| [**NVIDIA-DGX-Spark-with-vLLM**](https://github.com/NathanMaine/NVIDIA-DGX-Spark-with-vLLM) | End-to-end serving recipe for an 80B sparse MoE on one Spark, with per-user vs aggregate throughput stated honestly and confirmed by server-side accounting. | vLLM, CUDA, aarch64 |
| [**cmmc-training-data**](https://huggingface.co/datasets/Nathan-Maine/cmmc-training-data-2026-q2) | 18,747 curated compliance examples across 11 regulatory frameworks. Rebuilt from 67K raw examples (73% noise removed). | NIST, CMMC, HIPAA, FedRAMP |
| [**dgx-spark-kv-cache-benchmark**](https://huggingface.co/datasets/Nathan-Maine/dgx-spark-kv-cache-benchmark) | KV-cache quantization inference benchmarks on DGX Spark GB10 (q4/q8/f16 at long context). Published to r/LocalLLaMA, HN, NVIDIA Forums. | llama.cpp, CUDA 13.0, aarch64 |
| [**nv-ingest-document-pipeline**](https://github.com/NathanMaine/nv-ingest-document-pipeline) | GPU-accelerated PDF extraction on NVIDIA nv-ingest: any PDF corpus to chat-format JSONL training data, with a CPU-baseline benchmark harness. 61 tests, 95% coverage, mypy strict. | nv-ingest, Docker, Python |
| [**runpod-gpu-benchmark**](https://github.com/NathanMaine/runpod-gpu-benchmark) | 30-second GPU sanity check for rented pods (GEMM, memory bandwidth, GPU fingerprint). Named in RunPod's post-competition blog; related [containers PR #115](https://github.com/runpod/containers/pull/115) credited by the maintainer. | Shell, CUDA |
| [**governed-llm-gateway**](https://github.com/NathanMaine/governed-llm-gateway) | Policy-as-code LLM gateway: tamper-evident audit trails, rate limiting, cost telemetry. 103 tests. | Python, FastAPI |
| [**el-barto-serve**](https://github.com/NathanMaine/el-barto-serve) | OpenAI-compatible inference server. Auto-patches Flash Attention for Blackwell GPUs. | Python, PyTorch |
| [**memoriant-ops-bot**](https://github.com/NathanMaine/memoriant-ops-bot) | Multi-provider AI agent orchestration via Telegram/Matrix. Manages Claude Code, Codex CLI, Gemini CLI. | Python, WebSocket |

---

## OpenAI Parameter Golf

*Competition work is under my dentity007 handle (which displays as Nathan Maine).*

Training the best language model in 16MB on 8xH100s. Implemented all 7 of OpenAI's explicitly requested research directions, with 8 complete training scripts (11,810 lines of novel research code) and 95+ GPU experiments across RTX 5090, H100, and H200 SXM pods.

**Companion dashboard:** [parameter-golf-experiment-lab](https://github.com/NathanMaine/parameter-golf-experiment-lab), a [live interactive visualization](https://nathanmaine.github.io/parameter-golf-experiment-lab/) of 793+ scored community submissions with TTT-legality filtering, my 95+ experiment log, technique matrix, and cost analysis.

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

**Novel techniques developed beyond OpenAI's requests:** Adaptive Density Training (sparse-to-dense progressive unmasking), Echo Training (self-distillation from EMA checkpoints), Gradient Quilting (per-iteration adaptive LR with auto-freezing).

**Infrastructure built:** 486K+ chunk expert knowledge base from 80+ AI/ML experts. Competitive intelligence pipeline analyzing 1,084 competitor PRs. Multi-pod experiment orchestration. Full Hessian GPTQ validation on Hopper (H200 SXM).

---

## Agentic AI & Evaluation Systems

Deterministic, auditable agent components: evaluation, recovery, orchestration, and compliance enforcement.

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

---

## Compliance & Security Automation

Tools for scaling governance across distributed engineering teams in regulated environments (CMMC 2.0, NIST 800-171, HIPAA, FedRAMP, DFARS).

| Project | What It Does | Link |
| --- | --- | --- |
| **garak Contributions** | Homoglyph obfuscation prompts merged into NVIDIA garak's smuggling probe ([PR #1660](https://github.com/NVIDIA/garak/pull/1660), shipped in v0.15.0). Fabricated regulatory citation suite under review ([PR #1658](https://github.com/NVIDIA/garak/pull/1658)), architecture [Discussion #1659](https://github.com/NVIDIA/garak/discussions/1659). | [Repo](https://github.com/NathanMaine/garak-compliance-probes) |
| **Governed Voice Agent** | Policy-as-code governance, tamper-evident audit, and cost attribution for LiveKit voice agents, with a Doer/Judge governance eval suite | [Repo](https://github.com/NathanMaine/governed-voice-agent) |
| **Governance Graph Compiler** | Compiles policy Markdown into DAGs for deterministic audit evaluation | [Repo](https://github.com/NathanMaine/governance-graph-compiler) |
| **Patent Platform** | Full patent pipeline: search, analyze, draft, review, file. 706+ tests. | [Repo](https://github.com/NathanMaine/memoriant-patent-platform) |

---

## DevOps & Infrastructure

| Component | Details |
| --- | --- |
| **GPU Infrastructure** | NVIDIA DGX Spark (GB10, 128GB) for inference/training. 10G backbone, NFS-mounted NAS (3.6TB models). |
| **Distributed Training** | 8xH100 SXM on RunPod. torchrun DDP, torch.compile, FA3, GPTQ, zstd/Brotli compression. |
| **CI/CD & Automation** | GitHub Actions, launchd scheduling, automated replay archival, cron-based scraping pipelines. |
| **Observability** | GPU-accelerated knowledge-platform dashboard (FastAPI + Qdrant + SSE). GPU benchmarking scripts. Pod performance validation. |
| **Containerization** | Docker Compose for multi-service deployments. TensorRT-LLM containers for NVFP4 quantization. |

---

## Open Source Tutorials

Teaching ML by building from scratch. Free, fill-in-the-blanks format.

| Tutorial | What You Build | Link |
| --- | --- | --- |
| **smallest-ai-tutorial** | 4 neural networks from scratch in pure Python (MLP, LSTM, Transformer, BitNet) teaching phonics. 273 tests. | [Repo](https://github.com/NathanMaine/smallest-ai-tutorial) |
| **smallest-ai-built-from-the-ground-up** | Full project: Phase 1 complete with all 4 architectures, C export for ESP32, ARM QEMU verification. | [Repo](https://github.com/NathanMaine/smallest-ai-built-from-the-ground-up) |

---

## Claude Code Plugin Marketplace

[14 published plugins](https://github.com/NathanMaine/memoriant-marketplace) for AI-powered development workflows: architecture review, load testing, documentation drift detection, governance compilation, test coverage analysis, eval sandboxes, and more.

---

## Enterprise Delivery Background

| Domain | Proof Points |
| --- | --- |
| **Platform Scale** | $20M+ portfolios, 700K-user identity systems, multi-cloud (Sales/Service/Data Cloud) |
| **Cross-Team Execution** | Two 5/5 executive CSAT scores from Fortune 500 clients; SSO onboarding cut from 6 weeks to 2 (67%) |
| **Security & Identity** | ~200-application SSO program (Okta/SAML/OIDC) across federated business divisions |
| **Data Platforms** | 89M records across 28 source systems resolved into 45.9M unified profiles; match quality 87% to 95.48% |
| **Compliance** | SOC 2, PCI DSS, HIPAA, FERPA, and NIST 800-171 delivery across regulated engineering environments |
| **Regulated Environments** | Air-gapped AI deployment, CUI-handling systems, DFARS-adjacent compliance tooling |

---

**MIT Professional Education:** No Code AI and Machine Learning: Building Data Science Solutions | **Salesforce:** five certifications (Administrator, AI Associate, Data Cloud Consultant, Sales Cloud Consultant, Service Cloud Consultant) plus Financial Services Cloud Accredited Professional | **Scrum:** CSM | **AI Security & Governance** (Securiti) | **NVIDIA Inception** Member

📧 nmaine@gmail.com | [LinkedIn](https://www.linkedin.com/in/nathanmaine) | [HuggingFace](https://huggingface.co/Nathan-Maine)
