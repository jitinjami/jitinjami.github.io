---
layout: page
title: AI-Assisted Chronic Wound Assessment
description: Computer vision and smart-bandage sensing to track how chronic wounds heal, as part of the SWODDYS project.
img: assets/img/projects/wound.png
importance: 1
category: current
---

Chronic wounds such as venous and arterial ulcers heal slowly, and judging their progress still relies largely on subjective visual inspection.

In the <a href="https://www.mad.tf.fau.de/research/projects/swoddys-smart-wound-dressing-incorporating-dye-based-sensors/">SWODDYS project</a>, together with <a href="https://www.ukr.de/en/">Uniklinikum Regensburg</a> and <a href="https://www.presens.de">PreSens GmbH</a> and funded by the <a href="https://www.forschungsstiftung.bayern.de">Bayerische Forschungsstiftung</a>, I work on making that assessment objective. On the image side, I localise wounds and segment their tissue types with computer vision. On the sensing side, I analyse pH, O<sub>2</sub> and CO<sub>2</sub> readings from sensors inside the bandage to follow recovery over time.

{% include figure.html path="assets/img/projects/wound.png" alt="Tissue segmentation results of different models on a wound image" class="img-fluid rounded z-depth-1" %}
<div class="caption">
    Tissue segmentation of one wound by the ground-truth mask and eight benchmark models on the CicatrixVision (CiVi) dataset. The wound photo is hidden for patient privacy.
</div>

### Highlights

- Built the CicatrixVision (CiVi) dataset: 721 wound images from 66 patients, covering 5 wound types and annotated with 3 tissue classes.
- Benchmarked eight segmentation architectures on CiVi; the best, a UNet with an EfficientNet-B0 backbone, reaches a Dice score of 0.80.
- Used Grad-CAM to interpret what CNNs rely on when classifying venous and arterial ulcers.

### Outputs

- **Paper**: [Interpreting Venous and Arterial Ulcer Images Through the Grad-CAM Lens](https://www.mdpi.com/2075-4418/15/17/2184), *Diagnostics*, 2025.
- **Poster**: [Introducing the CicatrixVision (CiVi) Dataset: First steps into AI-assisted Chronic Wound Assessment]({{ '/assets/pdf/CiVi.pdf' | relative_url }}), MaD Conference 2025 and AI Day, University of Bayreuth 2025.
- **Poster**: [Exploring Correlation Between Tissue Composition and Healing in Chronic Wounds]({{ '/assets/pdf/AIBEConf_Jami.pdf' | relative_url }}), AIBE Conference 2024.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <a href="{{ '/assets/pdf/CiVi.pdf' | relative_url }}">{% include figure.html path="assets/img/projects/civi-poster.png" alt="CiVi dataset poster" class="img-fluid rounded z-depth-1" %}</a>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <a href="{{ '/assets/pdf/AIBEConf_Jami.pdf' | relative_url }}">{% include figure.html path="assets/img/projects/aibe-poster.png" alt="AIBE 2024 poster" class="img-fluid rounded z-depth-1" %}</a>
    </div>
</div>
<div class="caption">
    Left: CiVi dataset poster (MaD Conference and AI Day Bayreuth, 2025). Right: tissue composition poster (AIBE Conference, 2024). Click a poster to open the PDF.
</div>

### Student projects I supervised

- Alisha Mund: EDTRS Method for Generating Superpixels for Dermatological Wound Images
- Apu Das: Exploring Active Learning for Wound Tissue Segmentation
- Jule Lang: Evaluating Graph Neural Networks for Node Classification on Superpixel-Based Representations of Wound Images
- Ranganath Pujari: Superpixel-Based Wound Segmentation with Frozen Vision Foundation Models and Graph Neural Network Heads
