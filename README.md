# Awesome Persona-Aware Memory for LLM Agents

> A curated list of papers and resources on **persona / trait-aware long-term memory** for LLM-based agents — collected while preparing the *PsyMemo* AAAI 2027 submission.
> Inspired by [Neph0s/awesome-llm-role-playing-with-persona](https://github.com/Neph0s/awesome-llm-role-playing-with-persona).
> Last updated: **2026-05-12**

---

## Contents

- [Memory Consolidation Methods](#1-memory-consolidation-methods)
- [Long-Term Memory Benchmarks](#2-long-term-memory-benchmarks)
- [Personalization & Profiling Benchmarks](#3-personalization--profiling-benchmarks)
- [Role-Playing Agents (Persona × LLM)](#4-role-playing-agents-persona--llm)
- [Emotional Support & Personalized Generation](#5-emotional-support--personalized-generation)
- [Surveys & Position Papers](#6-surveys--position-papers)
- [Psychology Foundations](#7-psychology-foundations)
- [Industry Frameworks & Blogs](#8-industry-frameworks--blogs)

> **Legend**:
> 🌟 must-read for PsyMemo · 🧩 direct competitor · 🧱 backbone / dependency · 🧠 psychology grounding · 💼 industry baseline

---

## 1. Memory Consolidation Methods

- 🌟 🧩 **TiMem: Temporal-Hierarchical Memory Consolidation for Long-Horizon Conversational Agents**
  [[paper]](https://arxiv.org/abs/2601.02845) [[code]](https://github.com/TiMEM-AI/timem)
  *arXiv 2026.01* — SOTA on LoCoMo (75.30) and LongMemEval-S (76.88). 5-level temporal tree (Segment→Session→Day→Week→Profile). **Persona is the OUTPUT of consolidation, not an input.**

- 🧩 **EverMemOS: A Self-Organizing Memory Operating System for Structured Long-Horizon Reasoning**
  [[paper]](https://arxiv.org/abs/2601.02163) [[code]](https://github.com/EverMind-AI/EverOS)
  *arXiv 2026.01* — Reports SOTA on LoCoMo & LongMemEval; introduces PersonaMem v2 as **qualitative case study**.

- **Memory-R1: Reinforcement-Trained Sub-Agents for Add/Update/Delete Memory Ops**
  *Yan et al. arXiv 2026* — RL-trained black-box consolidation. Contrast to PsyMemo's white-box trait-grounded mapping.

- **Human-Like Remembering and Forgetting in LLM Agents**
  [[paper]](https://dl.acm.org/doi/10.1145/3765766.3765803)
  *ACM 2026 (corrected VoR)* — Cognitive-inspired memory; same spirit as PsyMemo's trait grounding.

- **Multi-Layered Memory Architectures for LLM Agents: An Experimental Study**
  [[paper]](https://arxiv.org/abs/2603.29194)
  *arXiv 2026.03* — Quantifies **persona consistency loss** as dialogue length grows. Strong PsyMemo motivation evidence.

- 🌟 🧱 **A-Mem: Agentic Memory for LLM Agents**
  [[paper]](https://arxiv.org/abs/2502.12110) [[code]](https://github.com/agiresearch/A-mem)
  *NeurIPS 2025* — Zettelkasten-style agentic note linking. **PsyMemo's backbone.**

- 🌟 💼 **Mem0: Building Production-Ready AI Agents with Scalable Long-Term Memory**
  [[paper]](https://arxiv.org/abs/2504.19413) [[code]](https://github.com/mem0ai/mem0)
  *ECAI 2025* — LoCoMo 91.6, LongMemEval 93.4. Production-grade SDK; personalization is a product feature, not a research operator.

- 🌟 **MemGPT: Towards LLMs as Operating Systems**
  [[paper]](https://arxiv.org/abs/2310.08560) [[code]](https://github.com/letta-ai/letta)
  *NeurIPS 2024 (Letta)* — Foundational virtual-context paper.

- **MemOS: A Memory Operating System for AI**
  [[code]](https://github.com/MemTensor/MemOS)
  *2025 → 2026 ongoing* — Self-evolving memory OS; claims 35% token savings. No trait-conditioned ablation.

---

## 2. Long-Term Memory Benchmarks

- 🌟 🧩 **From Recall to Forgetting: Benchmarking Long-Term Memory for Personalized Agents (Memora)**
  [[paper]](https://arxiv.org/abs/2604.20006)
  *arXiv 2026.04* — Weeks-to-months conversations; introduces **FAMA (Forgetting-Aware Memory Accuracy)**. Single-user; no cross-persona probe.

- 🌟 **Evaluating Very Long-Term Conversational Memory of LLM Agents (LoCoMo)**
  [[paper]](https://arxiv.org/abs/2402.17753) [[project]](https://snap-research.github.io/locomo/) [[code]](https://github.com/snap-research/locomo)
  *Snap Research 2024.02* — 10 conversations, ~26k tokens / 35 sessions each. **De facto** long-term memory benchmark.

- 🌟 **LongMemEval: Benchmarking Chat Assistants on Long-Term Interactive Memory**
  [[paper]](https://arxiv.org/abs/2410.10813)
  *arXiv 2024.10* — 500 sessions / ~1.5M tokens; 5 memory competencies.

- **MemoryAgentBench: Evaluating Memory in LLM Agents via Atomic Skills**
  [[code]](https://github.com/HUST-AI-HYZ/MemoryAgentBench)
  *ICLR 2026* — Personalization-oriented memory evaluation in agentic settings.

- **LongBench v2: Towards Deeper Understanding and Reasoning on Long Contexts**
  [[paper]](https://arxiv.org/abs/2412.15204) [[code]](https://github.com/THUDM/LongBench)
  *ACL 2025* — 8k–2M words; tests long-context models themselves, not external memory.

- **BEAM: Benchmark for Extra-long Agentic Memory (1M / 10M tokens)**
  *2025* — Tests ultra-long RAG-memory regimes.

---

## 3. Personalization & Profiling Benchmarks

- 🌟 🧩 **Know Me, Respond to Me: Benchmarking LLMs for Dynamic User Profiling and Personalized Responses at Scale (PersonaMem)**
  [[paper]](https://openreview.net/forum?id=6ox8XZGOqP)
  *Bowen Jiang, Dan Roth et al. — COLM 2025* — Multiple-choice profiling benchmark.

- **Enabling Personalized Long-term Interactions in LLM-based Agents through Persistent Memory and User Profiles**
  [[paper]](https://arxiv.org/abs/2510.07925)
  *arXiv 2025.10* — Framework + 5-day pilot user study (HCI flavor).

- **DuLeMon: Towards Dual Long-term Memory for Persona-Consistent Dialogue Generation**
  *Xu et al. 2022* — Early persona-consistent dialogue benchmark.

- **MemDaily: Daily-Life Personal Assistant Long-Term Memory**
  *Zhang et al. 2024*

---

## 4. Role-Playing Agents (Persona × LLM)

- 🧩 **PsyMem: Fine-grained Psychological Alignment and Explicit Memory Control for Advanced Role-Playing LLMs**
  [[paper]](https://arxiv.org/abs/2505.12814)
  *arXiv 2025.05* — **Name collision risk** ⚠️ — role-play consistency, not consolidation. PsyMemo must differentiate sharply.

- **CoSER: Coordinating LLM-Based Persona Simulation of Established Roles**
  *ICML 2025* — Currently strongest RPA framework on book characters.

- **ChARM: Character-based Act-adaptive Reward Modeling**
  [[paper]](https://arxiv.org/abs/2505.23923)
  *arXiv 2025.05* — RM for persona-consistent generation; orthogonal to memory.

- **PersonaEval: Are LLM Evaluators Human Enough to Judge Role-Play?**
  [[paper]](https://arxiv.org/abs/2508.10014)
  *arXiv 2025.08* — Meta-evaluation of LLM-judges in RPA.

- **Character-LLM: A Trainable Agent for Role-Playing**
  *EMNLP 2023* — RPA foundation paper.

- **MOA: Multi-Objective Alignment for Role-Playing Agents**
  [[paper]](https://arxiv.org/abs/2512.09756)
  *ACL 2026* — Multi-objective RL alignment; PsyMemo's interpretable-vs-RL counterpoint.

- **BookWorld: Book-Grounded Long-Horizon Role-Playing**
  *2025* — Long-horizon RPA evaluation.

---

## 5. Emotional Support & Personalized Generation

- **Kardia-R1 / KardiaBench: Personalized Empathetic Reasoning with RL**
  *2025* — Persona-conditioned RL for empathetic generation; **generation layer, not memory layer**.

- **SoulChat2.0 / PsyDT: Personalized Psychological Therapy Dialogue Model**
  *ACL 2025* — Counselor-style ESC with cognitive grounding.

- **CARE: Cognitive-reasoning Augmented RL for Emotional Support**
  [[paper]](https://arxiv.org/abs/2510.05122)
  *arXiv 2025.10* — CBT reasoning in single-turn ESC.

- **CoPoLLM: Cognitive Policy LLM for Emotional Support**
  *2025* — Psychology-grounded policy.

- **EmoHarbor: Long-Horizon Emotional Support Benchmark**
  *待补 — Topic 2 报告引用*

---

## 6. Surveys & Position Papers

- **Memory for Autonomous LLM Agents: Mechanisms, Evaluation, and Future Directions**
  [[paper]](https://arxiv.org/abs/2603.07670)
  *arXiv 2026.03* — Comprehensive survey; PsyMemo's taxonomy anchor.

- **Governing Evolving Memory in LLM Agents: Risks, Mechanisms, and Challenges**
  [[paper]](https://arxiv.org/abs/2603.11768)
  *arXiv 2026.03* — Position paper; cite as evidence the community is debating consolidation.

- **Awesome-Memory-for-Agents (TsinghuaC3I)**
  [[repo]](https://github.com/TsinghuaC3I/Awesome-Memory-for-Agents)
  *Continuously updated* — Most complete memory-for-agents paper list.

- **Agent-Memory-Paper-List (Shichun-Liu)**
  [[repo]](https://github.com/Shichun-Liu/Agent-Memory-Paper-List)
  *Continuously updated* — Sister taxonomy: Formation / Evolution / Retrieval.

- **Awesome-LLM-Role-Playing-with-Persona (Neph0s)**
  [[repo]](https://github.com/Neph0s/awesome-llm-role-playing-with-persona)
  *Continuously updated* — Layout inspiration for this list.

---

## 7. Psychology Foundations

> Each PsyMemo trait→operator mapping must cite ≥ 2 primary sources. Prefer originals over secondary reviews.

- 🧠 🌟 **Rusting, C. L.** *Personality, mood, and cognitive processing of emotional information: Three conceptual frameworks.* **Psychological Bulletin** 124(2), 165–196, **1998**.
  → High-N encoding bias toward negative information (`Φ_Encode.salience`).

- 🧠 **Bower, G. H.** *Mood and memory.* **American Psychologist** 36(2), 129–148, **1981**.
  → Foundational mood-congruent memory.

- 🧠 **Eysenck, M. W. & Eysenck, H. J.** *Learning, memory and personality.* **1981**.
  → N/E trait × memory retention.

- 🧠 **DeYoung, C. G.** *Personality neuroscience and the biology of traits.* **SPPC** 4(12), 2010.
  → Openness ↔ associative-thinking breadth (`Φ_Link.threshold`).

- 🧠 **Matthews, Deary & Whiteman.** *Personality Traits* (3rd ed.). **Cambridge University Press 2009**.
  → Authoritative trait theory review.

- 🧠 **Schwartz, S. H.** *Universals in the content and structure of values.* **Adv. Exp. Soc. Psych.** 25, **1992**.
  → Schwartz 10-values; half of PsyMemo's persona schema.

- 🧠 **McCrae & Costa.** *The Five-Factor theory of personality.* **2008**.
  → Canonical OCEAN reference.

- 🧠 **Soto, C. J. & John, O. P.** *The next Big Five Inventory (BFI-2).* **JPSP** 113(1), **2017**.
  → If using LLM-based BFI-2 self-report, cite this.

- 🧠 **Bluck, S. & Levine, L. J.** *Reminiscence as autobiographical memory.* **Ageing & Society** 18, **1998**.
  → Autobiographical memory consolidation theory.

---

## 8. Industry Frameworks & Blogs

- 💼 **Mem0** — [Site](https://mem0.ai) · [Blog: State of AI Agent Memory 2026](https://mem0.ai/blog/state-of-ai-agent-memory-2026) · [GitHub](https://github.com/mem0ai/mem0)
- 💼 **Letta** (formerly MemGPT) — [GitHub](https://github.com/letta-ai/letta)
- 💼 **MemOS** — [GitHub](https://github.com/MemTensor/MemOS)
- 💼 **EverMemOS / EverOS** — [GitHub](https://github.com/EverMind-AI/EverOS)
- 💼 **Supermemory** — single memory API with fact extraction + profile + selective forgetting
- 💼 **Zep / Graphiti** — temporal-graph memory with explicit timestamps
- 💼 **MemoBase**, **Nemori**, **LangMem** — alternative memory backends evaluated in Memora

---

## How to Use This List

| You want to ... | Read |
|----------------|------|
| Understand the **most threatening competitor** | §1: TiMem, Memora |
| Build the **backbone** | §1: A-Mem, MemGPT |
| Pick the **right benchmarks** | §2: LoCoMo, LongMemEval, Memora |
| Avoid **name collision** | §4: PsyMem (≠ PsyMemo) |
| Ground each **trait → operator** mapping | §7: Rusting 1998, DeYoung 2010, Schwartz 1992 |
| Defend against **"industry already did it"** rebuttal | §8: Mem0 / EverMemOS — note their qualitative-only personalization |

---

## Contributing

> This list lives in `@d:/Project/3090/reports/awesome-persona-memory.md`. To add a paper, append under the right section with the same format (emoji-tags + paper/code/project links + 1-line takeaway).

**Maintainer pipeline**:

1. Subscribe to arXiv RSS for cs.CL "memory" + cs.AI "agent" + "persona"
2. Re-check `TiMEM-AI/timem`, `agiresearch/A-mem`, `mem0ai/mem0`, `EverMind-AI/EverOS` every 2 weeks for v2 papers
3. Watch `TsinghuaC3I/Awesome-Memory-for-Agents`, `Shichun-Liu/Agent-Memory-Paper-List` for new additions

