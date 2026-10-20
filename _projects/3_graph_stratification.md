---
layout: page
title: HpStrat - Homophily-Aware Stratification
description: Building cross-validation folds for graph neural networks that balance node homophily, not just class labels, for more stable GNN evaluation.
img: assets/img/publication_preview/graph-strat.png
importance: 3
category: current
github: https://github.com/jitinjami/graph-strat
---

GNN accuracy on node classification can shift substantially from one random train/test split to another, which makes comparisons between architectures unreliable.
Stratifying by class, the usual remedy, is not enough on graphs: nodes are connected, and folds that differ in their mix of local neighbourhood homophily expose the model to systematically different conditions for message passing.

We propose **HpStrat**, a stratification procedure that uses node homophily as the primary axis and class label as the secondary one.
Across 15 node-classification datasets spanning the full homophily spectrum and 7 GNN architectures, it reaches a mean stability rank of 1.49, against 2.31 for random k-fold, and is the most stable method on 13 of the 15 datasets, while keeping class balance close to class-stratified splits.

{% include figure.html path="assets/img/publication_preview/graph-strat.png" alt="Random, class-stratified and HpStrat splits of the same graph" class="img-fluid rounded z-depth-1" %}
<div class="caption">
    The same graph split three ways. Random and class-stratified splits leave folds with different homophily; HpStrat balances both homophily and classes.
</div>

This extends our earlier work on [stratification for image segmentation](https://jitinjami.github.io/stratify/) to graphs.

**Accepted at the Learning on Graphs Conference (LoG) 2026.** [arXiv](https://arxiv.org/abs/2609.19210) · [Code](https://github.com/jitinjami/graph-strat)
