---
layout: page
title: Single-spiked complex Wishart matrices
description: Studied the distributions of two test statistics of centralized complex Wishart matrices with a single-spiked covariance structure
img: assets/img/rank1_wishart/trace_over_min.png
importance: 2
category: research
related_publications: eigenvalues, eigenvectors
---

In this project, we studied the properties of two important statistics of the complex Wishart ensemble, with a focus on the centralized (zero-mean) case with a single-spiked covariance structure. Formally, the ensemble can be defined as follows:

Let $$X \in \mathbb{C}^{n\times m} (m\geq n)$$ be a random matrix with independent columns, each distributed as complex multivariate Gaussian with zero mean and single-spiked covariance matrix, i.e., $$\mathbb{E}\left[X_j X_j^H\right] = \mathbf{I}_n+\eta u u^H$$ for $$j=1,2,\dots,m$$. Here, $$X_j$$ is the $$j^{\text{th}}$$ column of $$X$$, $$\mathbf{I}_n$$ is the $$n\times n$$ identity matrix, $$\eta$$ is a non-negative real constant, $$u\in\mathbb{C}^{n\times 1}$$ is an arbitrary non-random vector with unit Euclidean norm, and $$(.)^{H}$$ represents the Hermitian operator. 

Among various covariance structures, Johnstone’s spiked model [1] has been widely used in the literature to analyze the effects of having a few dominant trends or correlations in the covariance matrix, that are referred to as the spikes. These spikes arise in various practical scenarios in different scientific disciplines. For instance, they correspond to the first few dominant factors in factor models arising from financial economics first few principal components, the number of clusters in gene expression data, and the number of signals in signal detection and estimation etc.

Under this project, we first characterized the distributions of the Scaled Condition Number (SCN) defined as 
$$
    \kappa_{\text{SC}}^2(X) = \frac{\sum_{k=1}^n \lambda_k}{\lambda_1}
$$
where $$\lambda_k$$'s denote the ordered eigenvalues of $$XX^H$$, with $$\lambda_1$$ being the smallest. We were able to obtain an exact expression for the probability density function of the SCN, which was extended to an asymptotic result in the regime where $$m-n$$ stays constant while $$m,n\rightarrow \infty$$. The results were verified through various simulations, including ROC curves for blind detection in cognitive radio networks.

<div class="row">
    <div class="col-sm-8 mx-auto d-block mt-3 mt-md-0">
        {% include figure.html path="assets/img/rank1_wishart/trace_over_min.png" title="example image" class="img-fluid rounded" %}
    </div>
</div>
<div class="caption">
    Comparison of simulated data points and the analytical p.d.f
</div>

<div class="row">
    <div class="col-sm-8 mx-auto d-block mt-3 mt-md-0">
        {% include figure.html path="assets/img/rank1_wishart/roc_curve.png" title="example image" class="img-fluid rounded" %}
    </div>
</div>
<div class="caption">
    Probability of detection versus false alarm probability; ROC curves are shown for $$m=n=4$$
</div>

Next, we focused on the properties of the eigenvectors of centralized single-spiked complex Wishart matrices. Accordingly, the distributions of the test statistics $$Z_k^{(n)}=\mid u^Hv_k \mid^2$$ were studied, where $$v_k$$ denotes the $$k^{\text{th}}$$ eigenvector of $$XX^H$$. Specifically, we focused on the cases $$k=1$$ and $$k=n$$. The results were verified through simulations as before, including quantile-quantile plots for theoretical and empirical quantiles, which demonstrate the agreement better in-case of highly skewed distributions such as the ones observed here.

<div class="row">
    <div class="col-sm-8 mx-auto d-block mt-3 mt-md-0">
        {% include figure.html path="assets/img/rank1_wishart/max_eigvector.png" title="example image" class="img-fluid rounded" %}
    </div>
</div>
<div class="caption">
    Comparison of simulated data points and the analytical p.d.f.
</div>

<div class="row">
    <div class="col-sm-8 mx-auto d-block mt-3 mt-md-0">
        {% include figure.html path="assets/img/rank1_wishart/max_eigvec_qqplot.png" title="example image" class="img-fluid rounded" %}
    </div>
</div>
<div class="caption">
    Quantile-quantile plots - sample quantiles vs theoretical quantiles
</div>

All the simulations corresponding to these studies were carried-out using Mathematica. The notebooks can be found on Github at: [github.com/pasandissanayake/single-spiked-wishart](https://github.com/pasandissanayake/single-spiked-wishart)

[1] I. M. Johnstone, “On the distribution of the largest eigenvalue in principal components analysis,” Ann. Statist., vol. 29, no. 2, pp. 295–327, Apr. 2001.