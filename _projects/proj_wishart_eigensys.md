---
layout: page
title: Properties of centralized complex Wishart matrices with rank-1 correlation structure
description: Studied the properties (distributions corresponding to statistics) of centralized complex Wishart matrices with a rank-1 correlation structure
img: assets/img/rank1_wishart/trace_over_min.png
importance: 2
category: research
related_publications: eigenvalues, eigenvectors
---

In this project, we studied the properties of two important statistics of the complex Wishart ensemble, with a focus on the centralized (zero-mean) case with a rank-1 covariance structure. Formally, the ensemble can be defined as follows:

Let $$X \in \mathbb{C}^{n\times n} (m\geq n)$$ be a random matrix with independent columns as 

Among various covariance structures, Johnstone’s spiked model [38] has been widely used
in the literature to analyze the effects of having a few dominant trends or correlations in the
covariance matrix. To be precise, under this setting, the covaraince matrix Σ ∈ Cn×n of X
is modeled as Σ = In + ∑r
k=1 θkuku∗
k, where In is the n × n identity matrix, uk ∈ Cn×1,
k = 1, 2, . . . , r(≤ n) are a set of orthonormal vectors, and θ1 ≥ θ2 ≥ . . . ≥ θr ≥ 0. Consequently,
the uks’ are referred to as the spikes and this particular covariance structure is sometimes known
as rank-r perturbation of the identity matrix. This fact is further highlighted by the eigen-
structure of Σ in which the the dominant r eigenvalues can be written as, θ1 + 1 ≥ θ2 + 1 ≥
. . . ≥ θr + 1, whereas the rest of the n − r eigenvalues assume 1. These spikes arise in various
practical scenarios in different scientific disciplines. For instance, they correspond to the first few
dominant factors in factor models arising from financial economics [39]–[41], first few principal
2The quantity κ−2
SC (X) is known as the minimum eigenvalue of the fixed trace Wishart-Laguerre ensemble in the statistical
physics literature; see e.g [19]–[25] and references therein.
June 1, 2022 DRAFT
4
components [38], [42], the number of clusters in gene expression data [43], and the number of
signals in signal detection and estimation, see e.g., [44]–[54], and references therein. In particular,
[45] and [47] have focus on the rank-r model, whereas the rank-1 (i.e., single-spiked) model,
which is of our interest in this manuscript, has been employed by [46], [48]–[55] in the signal
detection problem. In a sharp contrast, Hanlen and Grant [56] have used the rank−r model
to investigate the effect of correlation on the MIMO capacity. Be that as it may, the constant
correlation model, which is one of the most important correlation models frequently used in a
wide array of MIMO applications [57]–[62], gives rise to a single spiked model for the scaled Σ
matrix. To be specific, under this setting, Σ consists of 1’s in the main diagonal and σ ∈ [0, 1)’s
in all off-diagonal entries. As such, 1
1−σ Σ admits the desired single spiked structure given by
1
1−σ Σ = In + nσ
1−σ 11∗, where 1 =
( 1√n
1√n . . . 1√n
)∗
. For instance, this has been exploited
in [57], [58] to derive certain performance measures related to MIMO systems. Moreover, the
SCN has been used as a performance metric in several wireless signal processing applications
involving MIMO systems as delineated in [27], [29], [30]. Therefore, these facts further highlight
the utility of the single spiked covariance model in a wide class of applications.
The square of the SCN κ2
SC(X) in conjunction with correlated Gaussian X having a sing