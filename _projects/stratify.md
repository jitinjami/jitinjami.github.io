---
layout: page
title: Stratification for Image Segmentation
description: Label-aware dataset splitting for image segmentation, giving more representative test sets and more stable model evaluation.
img: assets/img/publication_preview/stratify.png
importance: 2
category: current
github: https://github.com/jitinjami/SemanticStratification
---

Random splits of segmentation datasets often produce unrepresentative test sets, which biases evaluation. Stratified sampling solves this for classification, but segmentation is harder: every image carries several labels, usually with strong class imbalance.

We introduce **Iterative Pixel Stratification (IPS)**, a simple label-aware sampling method for segmentation, and **Wasserstein-Driven Evolutionary Stratification (WDES)**, a genetic algorithm that minimises the Wasserstein distance between the label distributions of the splits.

{% include figure.html path="assets/img/publication_preview/stratify.png" alt="Ideal and random splits of PascalVOC plane images" class="img-fluid rounded z-depth-1" %}
<div class="caption">
    PascalVOC images of the class "plane". An ideal split balances the classes across folds; random splitting does not guarantee this.
</div>

### Highlights

- WDES is provably globally optimal given enough generations.
- Using new statistical heterogeneity metrics, WDES consistently produces more representative splits than random sampling.
- Across street scenes, medical imaging and satellite imagery, WDES lowers performance variance and improves model evaluation.
- The gains are largest on small, imbalanced and low-diversity datasets, where conventional splitting is most prone to bias.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/stratify-delta.png" alt="Relative improvement of WDES over random splitting" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Relative improvement of WDES over random splitting. The gap shrinks with more classes, but WDES keeps an edge on datasets with high class ubiquity.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/stratify-entropy.png" alt="Stratification method rankings by performance variance" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Method rankings by performance variance. WDES ranks highest in low-entropy settings; random splitting catches up as entropy grows.
</div>
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/stratify-runtime.png" alt="Runtime of random splitting, IPS and WDES" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Runtime of random splitting, IPS and WDES across all datasets.
</div>

### Outputs

- **Paper**: [Stratify or Die: Rethinking Data Splits in Image Segmentation](https://openreview.net/pdf?id=ngtFOxkQ8b), NeurIPS 2025. [arXiv](https://arxiv.org/abs/2509.21056)
- **Code**: [jitinjami/SemanticStratification](https://github.com/jitinjami/SemanticStratification)
- **Poster**: [NeurIPS 2025, San Diego]({{ '/assets/pdf/stratify_poster.pdf' | relative_url }})

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <a href="{{ '/assets/pdf/stratify_poster.pdf' | relative_url }}">{% include figure.html path="assets/img/projects/stratify-poster.png" alt="Stratify or Die poster" class="img-fluid rounded z-depth-1" %}</a>
    </div>
</div>
<div class="caption">
    NeurIPS 2025 poster. Click to open the PDF.
</div>
