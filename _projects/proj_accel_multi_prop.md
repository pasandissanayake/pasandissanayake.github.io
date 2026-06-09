---
layout: page
title: Accelerating Multi-Property Molecular Design via Counterfactual Explanations
description: Proposed FINDER, a unified framework for composite molecular inverse design that efficiently finds molecular candidates satisfying multiple target properties simultaneously using entropic-risk-based counterfactual explanations and projected gradient descent.
img: assets/img/accel_multi_prop/finder_overview.png
importance: 1
category: research
related_publications: finderMolecular, robustCF
---

Inverse design of composite molecular structures is computationally expensive due to vast search spaces. The challenge is further exacerbated when the desired molecule must simultaneously satisfy multiple properties—for instance, biopolymer nanocomposites as sustainable plastic alternatives need to meet criteria like mechanical strength, biodegradability, and optical transparency simultaneously. Existing techniques often focus on one property at a time and rely on computationally expensive genetic algorithms or perturbation-based optimization.

We propose **FINDER** (Fast INverse Design via Entropic-Risk-Based Counterfactual Explanations), a unified framework for composite molecular design that efficiently discovers candidates satisfying multiple target properties. FINDER brings several innovations:

- **Multi-property counterfactual optimization**: A novel constrained optimization for finding counterfactual explanations that satisfy multiple target properties simultaneously.
- **Entropic risk tuning knob**: A flexible parameter $$\theta$$ that balances different properties via entropic risk measures, avoiding worst-case min-max optimization.
- **Fast projected gradient descent**: An iterative solver that is orders of magnitude faster than genetic algorithms or Bayesian optimization.

<div class="row">
    <div class="col-sm-8 mx-auto d-block mt-3 mt-md-0">
        {% include figure.html path="assets/img/accel_multi_prop/finder_overview.png" title="FINDER overview" class="img-fluid rounded" %}
    </div>
</div>
<div class="caption">
    FINDER alters both compositions and functional groups in biopolymer nanocomposites, finding new derivatives that satisfy multiple desirable properties of sustainable plastics simultaneously—within seconds.
</div>

FINDER uses a unified input representation based on molecular fingerprints that supports permutation-invariant predictions and enables modifications to both molecular structures and constituent ratios. The framework also provides theoretical guarantees on the fraction of properties satisfied by generated counterfactuals.

<div class="row">
    <div class="col-sm mx-auto d-block mt-3 mt-md-0">
        {% include figure.html path="assets/img/accel_multi_prop/hea_counterfactual.png" title="HEA counterfactual example" class="img-fluid rounded" %}
    </div>
</div>
<div class="caption">
    Example counterfactual generation for the High Entropy Alloy (HEA) dataset: FINDER identifies minimal changes in alloy compositions to satisfy seven target properties simultaneously.
</div>

We evaluate FINDER on two applications: (i) High Entropy Alloy (HEA) design with 7 target properties, and (ii) biopolymer nanocomposite design with 8 target properties. FINDER achieves a superior trade-off between generation time and number of properties satisfied compared to genetic algorithms, NSGA-II, and Bayesian optimization baselines—reducing counterfactual generation time from hours to seconds.
