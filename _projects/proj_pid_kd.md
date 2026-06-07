---
layout: page
title: Quantifying Knowledge Distillation Using Partial Information Decomposition
description: Proposed information-theoretic metrics based on Partial Information Decomposition (PID) to quantify and explain knowledge transfer in distillation. This led to the Redundant Information Distillation (RID) framework, which filters task-irrelevant information and improves distillation under nuisance teachers.
img: assets/img/pid_kd/rid_framework.png
importance: 1
category: research
related_publications: knowledgeDistill2
---

<h1>Quantifying Knowledge Distillation Using Partial Information Decomposition</h1>

Knowledge distillation compresses complex machine learning models by training a smaller student model to emulate the representations of a larger teacher model. However, the teacher's representations may also encode nuisance information irrelevant to the downstream task. Distilling such irrelevant information can impede the performance of a capacity-limited student. This raises a fundamental question: *What are the information-theoretic limits of knowledge distillation?*

We leverage Partial Information Decomposition (PID) to formally define and quantify:
- **Knowledge to distill** (*unique information*): the task-relevant information in the teacher that is not yet captured by the student.
- **Transferred knowledge** (*redundant information*): the task-relevant information that is common between the teacher and the student.

We theoretically demonstrate that the task-relevant transferred knowledge is succinctly captured by the redundant information about the task between the teacher and student, and show through examples that existing frameworks based on maximizing mutual information $$I(T;S)$$ between teacher and student representations have fundamental limitations—they force the student to blindly mimic the teacher regardless of task-relevance.

<div class="row">
    <div class="col-sm-8 mx-auto d-block mt-3 mt-md-0">
        {% include figure.html path="assets/img/pid_kd/rid_framework.png" title="RID framework" class="img-fluid rounded" %}
    </div>
</div>
<div class="caption">
    Redundant Information Distillation (RID) framework: A multi-level optimization that maximizes a lower bound on the transferred knowledge (redundant information) as a regularizer during distillation.
</div>

Based on these insights, we propose **Redundant Information Distillation (RID)**—a novel multi-level optimization framework that maximizes redundant information as a regularizer. RID precisely captures task-relevant knowledge and filters out the task-irrelevant information from the teacher. Unlike prior methods, RID is resilient to nuisance teachers (untrained or uninformative teachers) where conventional distillation methods degrade student performance.

<div class="row">
    <div class="col-sm mx-auto d-block mt-3 mt-md-0">
        {% include figure.html path="assets/img/pid_kd/cifar10_results.png" title="CIFAR-10 results" class="img-fluid rounded" %}
    </div>
</div>
<div class="caption">
    Classification accuracy on CIFAR-10: RID maintains strong performance under both trained and untrained teachers, while VID degrades significantly under an uninformative teacher.
</div>

Our experiments on CIFAR-10, CIFAR-100, and a transfer learning setup (ImageNet → CUB-200-2011) confirm that RID outperforms existing approaches, particularly in scenarios where the teacher encodes substantial nuisance information.

<b>Github:</b> [https://github.com/pasandissanayake/kd-rid](https://github.com/pasandissanayake/kd-rid)
