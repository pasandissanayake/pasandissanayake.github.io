---
layout: page
title: Counterfactual Explanations and Model Extraction Attacks
description: Explored how the additional information provided by counterfactual explanations can be exploited by an adversary in-order to improve model extraction attacks
img: assets/img/12.jpg
importance: 1
category: research
related_publications: 
---

Counterfactual explanations provide guidance on achieving a favorable outcome from a model, with minimum input perturbation. However, they can also be exploited to leak information about the underlying model, causing privacy concerns. Prior work shows that one can query for counterfactuals with several input instances and train a surrogate model using all the queries and their counterfactuals. In this project, we investigate how model extraction attacks can be improved by further leveraging the fact that the counterfactuals also lie quite close to the decision boundary.

As it turned-out, proposed model extraction attack surpassed the performance of the baseline attack in "Ulrich Aïvodji, Alexandre Bolot, and Sébastien Gambs. Model extraction from counterfactual explanations. arXiv preprint arXiv:2009.01884, 2020" in a wide array of experiments. 
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/counterf_me/2d_demo.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/counterf_me/2d_demo.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>

This project was supported by Northrop Grumman Corporation.

