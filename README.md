# Mahdi Mostajabdaveh

**Principal OR/AI Scientist at Kinaxis · AI research and technical leadership**

I develop AI systems that reason about complex problems, discover better algorithms, and improve the way decisions are made. My work sits at the intersection of language models, multi-agent systems, mathematical optimization, and large-scale decision support. I care about methods that can be tested carefully and then used repeatedly in a real system.

At Kinaxis, I lead AI acceleration for a production optimization solver and the evaluation infrastructure for coding agents that modify it. This work involves more than generating code. An agent has to make a change, preserve solver correctness, and produce a measurable improvement on the workloads that matter. I am building the research and engineering loop that makes those judgments possible.

Before Kinaxis, I was Senior Staff Researcher and AI Lead for Huawei's OptVerse solver. I led research on AI for optimization, helped deliver a routing engine used by more than 20 enterprise customers, and developed OptvEvolve, an LLM-driven framework for evolving and tuning optimization algorithms. Our OptVerse-CityU team placed first in the 2026 CVRPLIB Best Known Solutions Challenge, producing 51 new best-known solutions on large vehicle-routing instances.

[Website](https://mahdims.github.io/) · [Research](https://mahdims.github.io/research.html) · [Publications](https://mahdims.github.io/publications.html) · [Google Scholar](https://scholar.google.com/citations?user=TKmUJokAAAAJ&hl=en) · [LinkedIn](https://www.linkedin.com/in/mahdi-mostajabdaveh/) · [Email](mailto:mahdi.ms86@gmail.com)

## What I study

The common thread in my research is the connection between an intelligent proposal and a reliable test. A language model can suggest a model, a search action, a heuristic, or a piece of solver code. The important question is how to evaluate that proposal before it is trusted. Depending on the problem, the test may be a feasibility check, an objective value, a mathematical bound, a benchmark, an expert judgment, or performance on held-out instances.

This perspective leads to research that is both methodological and applied. I design learning and search procedures, build the benchmarks and evaluation harnesses needed to measure them, and work with the constraints of production software. Exact optimization is useful here because it gives a precise language for asking whether a generated object is valid and whether it improves the decision being optimized.

## Research programs

| Program | Question | Representative work |
| --- | --- | --- |
| **Agent reasoning and adaptation** | How can an agent improve its decisions through process feedback, memory, and inference-time search? | [MASPRM](https://github.com/milad1378yz/MASPRM), [SEDIMA](https://openreview.net/forum?id=6hbm4tnWBl) |
| **Automated algorithm discovery and learned search** | How can AI generate algorithms and learn where to search? | [EvoCut](https://github.com/milad1378yz/EvoCut), [Latent Heuristic Search](https://github.com/cheikh025/LHS), [COAgents](https://github.com/mahdims/COAgents) |
| **Language, modeling, and evaluation** | How can language models construct formal models and be tested on technical reasoning? | [ORQA](https://github.com/nl4opt/ORQA), [NL4Opt](https://github.com/nl4opt/nl4opt-competition), [SmartAPS](https://arxiv.org/abs/2507.17927) |
| **Optimization methods and decision systems** | How can exact, heuristic, and accelerated methods improve constrained decisions? | [AILS-Enhanced](https://github.com/mahdims/AILS-Enhanced), [Branch-and-price](https://github.com/mahdims/Branch-and-price-), [Bayan](https://github.com/saref/bayan) |

## Research contributions

### Process feedback for agent reasoning

[MASPRM](https://github.com/milad1378yz/MASPRM) studies process reward models for multi-agent systems. Rather than scoring only the final answer, the model scores intermediate messages and gives search procedures a signal about which step is promising or has gone wrong. The resulting step-level beam search and Monte Carlo tree search connect learned judgment with a structured search procedure.

[SEDIMA](https://openreview.net/forum?id=6hbm4tnWBl) studies memory for search agents. The goal is to carry useful experience across runs so that a system can improve its decisions without updating the underlying model after every attempt. This line of work asks what should be stored, how it should be retrieved, and how memory should affect a search policy.

### AI that discovers algorithms

[EvoCut](https://github.com/milad1378yz/EvoCut) uses evolutionary search and language models to discover acceleration cuts for mixed-integer programs. The candidate is not judged by how plausible its explanation sounds. It is translated into an executable form and evaluated through solver experiments.

[Latent Heuristic Search](https://github.com/cheikh025/LHS) explores continuous optimization for automated algorithm design. [COAgents](https://github.com/mahdims/COAgents) learns control over different decisions in vehicle-routing search, including node selection, move selection, and jump decisions. Together, these projects examine different ways to search over algorithms and search policies rather than treating the solver as a fixed black box.

### Language to formal decision models

I have worked on the full path from natural-language specifications to executable optimization models. The [NL4Opt competition](https://github.com/nl4opt/nl4opt-competition) established a benchmark and shared tasks for translating problem descriptions into optimization representations. [LaTeX2Solver](https://mahdims.github.io/publications.html#latex2solver) and the multi-agent modeling framework published in INFOR study how systems can construct, inspect, and revise formal models. [ORQA](https://github.com/nl4opt/ORQA) evaluates whether language models can apply operations-research knowledge and perform multistep reasoning. [SmartAPS](https://arxiv.org/abs/2507.17927) connects language models with tools for operations-management decision support.

### Optimization in practice

My earlier work includes exact and heuristic methods for routing, humanitarian logistics, community detection, cutting and scheduling, quantization, tomography, and filter design. The [Branch-and-price implementation](https://github.com/mahdims/Branch-and-price-) supports research on equitable last-mile relief distribution. [AILS-Enhanced](https://github.com/mahdims/AILS-Enhanced) is associated with our CVRPLIB Challenge entry. These projects keep the algorithmic questions grounded in the details that determine whether a method is useful: runtime, memory, solution quality, reproducibility, and the behavior of the implementation on difficult instances.

## From research to systems

I enjoy the part of applied science where an idea has to survive contact with an existing codebase. At Huawei, OptvEvolve turned algorithm design from a manual cycle that could take weeks into an executable process that could be tested and iterated more quickly. At Kinaxis, I am applying the same discipline to AI-assisted changes in a production solver. The evaluation harness checks correctness and performance before a change can be treated as an improvement.

The work also changes how I lead. A research direction needs a clear claim, a test that could falsify it, and an artifact that another person can inspect. A production system adds operational constraints, customer workloads, integration costs, and maintenance. I try to keep those concerns visible from the start so that a paper, a benchmark, and a deployed component support the same technical story.

## Selected work

| Project | Contribution | Evidence |
| --- | --- | --- |
| **[MASPRM](https://github.com/milad1378yz/MASPRM)** | Process reward model for intermediate multi-agent messages and step-level search. | [Paper](https://arxiv.org/abs/2510.24803) |
| **[EvoCut](https://github.com/milad1378yz/EvoCut)** | Evolution-guided discovery of reusable acceleration cuts for mixed-integer programs. | [Paper](https://arxiv.org/abs/2508.11850) · [Project page](https://milad1378yz.github.io/EvoCut/) |
| **[ORQA](https://github.com/nl4opt/ORQA)** | Benchmark for expert operations-research knowledge and multistep modeling reasoning. | [AAAI 2025 paper](https://arxiv.org/abs/2412.17874) |
| **[COAgents](https://github.com/mahdims/COAgents)** | Learned control over node, move, and jump decisions in vehicle-routing search. | [LION 20 paper](https://arxiv.org/abs/2605.20618) |
| **[Latent Heuristic Search](https://github.com/cheikh025/LHS)** | Continuous latent-space optimization for automated algorithm design. | [LION 20 paper](https://arxiv.org/abs/2605.17137) |
| **[AILS-Enhanced](https://github.com/mahdims/AILS-Enhanced)** | Multi-start AILS-II implementation associated with our CVRPLIB Challenge entry. | [Challenge result](https://galgos.inf.puc-rio.br/cvrplib/index.php/en/bks_challenge/score/) |
| **[NL4Opt](https://github.com/nl4opt/nl4opt-competition)** | Benchmark, dataset, and shared tasks for natural-language optimization modeling. | [NeurIPS competition paper](https://proceedings.mlr.press/v220/ramamonjison23a.html) |

## Background

I earned my Ph.D. in operations research at Koç University and completed a postdoctoral fellowship with Prof. Michel Gendreau at Polytechnique Montréal and CIRRELT. My publication record includes work at NeurIPS, AAAI, ACL, EJOR, INFOR, and IISE Transactions, as well as multiple filed patents.

For the complete record, see my [publications](https://mahdims.github.io/publications.html), [systems](https://mahdims.github.io/projects/), and [Google Scholar profile](https://scholar.google.com/citations?user=TKmUJokAAAAJ&hl=en).
