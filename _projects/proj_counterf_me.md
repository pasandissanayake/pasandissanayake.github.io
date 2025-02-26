---
layout: page
title: Counterfactual Explanations and Model Extraction Attacks
description: Explored how the additional information provided by counterfactual explanations can be exploited by an adversary in-order to improve model extraction attacks
img: assets/img/counterf_me/2d_demo.png
importance: 1
category: research
related_publications: counterfME
---

<div class="row">
    <div class="col-sm-8 mx-auto d-block mt-3 mt-md-0">
        {% include figure.html path="assets/img/counterf_me/mlaas_model.png" title="example image" class="img-fluid rounded" %}
    </div>
</div>
<div class="caption">
    Problem setting
</div>

Counterfactual explanations provide guidance on achieving a favorable outcome from a model, with minimum input perturbation. However, they can also be exploited to leak information about the underlying model, causing privacy concerns. Prior work has shown that one can query for counterfactual explanations with several input instances and train a surrogate model using all the queries and their counterfactual explanations. In this project, we investigate how model extraction attacks can be improved by further leveraging the fact that the counterfactual explanations also lie quite close to the decision boundary.

The proposed attack mitigates the issue of decision boundary shift, which is a problem that occurs in case of systems that provide counterfactual explanations for queries originating only from one side of the target model's decision boundary.
<div class="row">
    <div class="col-sm-8 mx-auto d-block mt-3 mt-md-0">
        {% include figure.html path="assets/img/counterf_me/boundary_shift.png" title="example image" class="img-fluid rounded" %}
    </div>
</div>
<div class="caption">
    Decision boundary shift issue
</div>

Consequently, the proposed model extraction attack surpassed the performance of the baseline attack in [1] in a wide array of experiments.
<div class="row">
    <div class="col-sm mx-auto d-block mt-3 mt-md-0">
        {% include figure.html path="assets/img/counterf_me/2d_demo.png" title="example image" class="img-fluid rounded" %}
    </div>
</div>
<div class="caption">
    2D demonstration of the proposed attack. Notice how the decision boundary of the surrogate model obtained by the baseline attack has shifted, but the proposed attack has mitigated this shift.
</div>

<div class="row">
    <div class="col-sm mx-auto d-block mt-3 mt-md-0">
        {% include figure.html path="assets/img/counterf_me/real_mccf_fidelity.png" title="example image" class="img-fluid rounded" %}
    </div>
</div>
<div class="caption">
    Performance (measured as fidelity) of the proposed and baseline attacks over real-world data
</div>

This project was supported by Northrop Grumman Corporation.

<b>Github:</b> [https://github.com/pasandissanayake/model-reconstruction-using-counterfactuals](https://github.com/pasandissanayake/model-reconstruction-using-counterfactuals)

[1] Ulrich Aïvodji, Alexandre Bolot, and Sébastien Gambs, "Model extraction from counterfactual explanations," arXiv preprint arXiv:2009.01884, 2020.
