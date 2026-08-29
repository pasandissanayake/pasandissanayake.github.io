---
layout: page
title: MAPLEBench — A Benchmark for Multi-Agent Privacy in Long-Horizon Executions
description: MAPLEBench evaluates privacy leakage in realistic long-horizon multi-agent workflows. Built from 51 ALE benchmark tasks with injected sensitive information, sandboxed tool environments, adversarial third-party agents, and a dual detection framework (Disclosure Detector + Leakage Estimator).
img: assets/img/privacy_benchmark/benchmark_overview.png
importance: 1
category: research
related_publications: maplebench
---

MAPLEBench introduces a benchmark for evaluating privacy leakage in realistic long-horizon, multi-agent workflows. The benchmark consists of 51 tasks derived from the Agents' Last Exam (ALE) benchmark, with sensitive information injected through task descriptions, structured data, and unstructured files. Agents operate in a sandboxed Ubuntu Docker container with 13 real tools, while multi-agent settings expose them to adversarial third-party agents that attempt to extract sensitive information through manipulated tool responses.

<div class="row">
    <div class="col-sm-8 mx-auto d-block mt-3 mt-md-0">
        {% include figure.html path="assets/img/privacy_benchmark/benchmark_overview.png" title="MAPLEBench benchmark overview" class="img-fluid rounded" %}
    </div>
</div>
<div class="caption">
    MAPLEBench architecture: Tasks modified from ALE with injected sensitive information. Agents execute in a sandboxed VM with real tools. Multi-agent settings wrap output-modifying tool calls with adversarial third-party agents. Detection combines a three-tier Disclosure Detector with an information-theoretic Leakage Estimator and contextual integrity evaluation.
</div>

## Key Findings

- **Privacy-enhancing instructions do not consistently reduce leakage** — they help some models (GPT-5.6-sol, Grok-4.3) but **exacerbate** leakage for DeepSeek-v3.2 by making it aware of actual sensitive data in context.

- **Privacy-utility trade-off** — moderate, highly significant positive correlation between task performance and privacy violations (Spearman ρ=0.335, p=3.16×10⁻²⁰).

- **Dormancy effects** — over 25% of sensitive atoms remain undetected for more than half the trajectory; semantic information stays dormant significantly longer than syntactic.

- **Strong detector agreement** — Disclosure Detector shows Cohen's κ=0.84 across LLM judges; Leakage Estimator agrees with Detector at κ=0.76 (88% agreement on valid questions).
