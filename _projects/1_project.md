---
layout: page
title: "CaReAQA: A Cardiac and Respiratory Audio Question Answering Model for Open-Ended Diagnostic Reasoning"
description: "A question-answering model designed to enable large language models to perform diagnostic reasoning over auscultation audio recordings from real-world clinical data."
img: assets/img/careaqa1.jpg
importance: 1
category: work
related_publications: true
---

CaReAQA is an open-ended audio question answering model designed to enable large language models to reason over real-world auscultation recordings of heart and lung sounds. Unlike traditional diagnostic systems that rely on predefined labels or closed-form outputs, CaReAQA generates free-form diagnostic responses to open-ended clinical questions, closely resembling human clinical reasoning.

The model combines a self-supervised medical audio encoder with a language model by aligning both modalities in a shared latent space. This enables it to interpret subtle audio features—such as murmurs, crackles, and timing patterns—and integrate them with the semantic content of diverse clinical queries.

To support development and evaluation, we introduce a benchmark dataset of cardiac and respiratory recordings paired with natural language questions that reflect real diagnostic workflows. CaReAQA demonstrates strong qualitative and quantitative performance in generating accurate, interpretable responses, making it a promising step toward audio-based clinical decision support.

<div class="row mt-4">
  <div class="col-sm-12">
    {% include figure.liquid path="assets/img/careaqa.jpg" title="Overview of the CaReAQA framework." class="img-fluid rounded z-depth-1" %}
  </div>
</div>

<div class="caption">
  Overview of the CaReAQA model pipeline. The system encodes auscultation audio and a clinical question into a shared latent space, which is then decoded by a language model to produce free-form answers.
</div>

<div class="row mt-4">
  <div class="col-sm-12">
    {% include figure.liquid path="assets/img/examples.png" title="Example question types and model responses." class="img-fluid rounded z-depth-1" %}
  </div>
</div>

<div class="caption">
  Example question types paired with answers.
</div>

<div class="row mt-4">
  <div class="col-sm-12">
    {% include figure.liquid path="assets/img/eval.png" title="Performance across multiple QA tasks." class="img-fluid rounded z-depth-1" %}
  </div>
</div>

<div class="caption">
  Evaluation results showing CaReAQA’s performance on open-ended audio task.
</div>

