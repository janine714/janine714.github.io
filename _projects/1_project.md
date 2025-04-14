---
layout: page
title: "CaReAQA: A Cardiac and Respiratory Audio Question Answering Model for Open-Ended Diagnostic Reasoning"
description: "A question-answering model designed to enable large language models to perform diagnostic reasoning over auscultation audio recordings from real-world clinical data."
img: assets/img/careaqa1.jpg
importance: 1
category: work
related_publications: true
---

CaReAQA is a novel question-answering model that enables large language models to reason over auscultation audio. It tackles the complex task of interpreting real-world heart and lung sounds and generating diagnostic responses to open-ended clinical questions. Unlike traditional diagnostic classifiers or rule-based expert systems, CaReAQA is designed to handle free-form queries in a flexible and interpretable manner, closely mirroring human diagnostic reasoning.

We introduce a benchmark comprising real-world auscultation recordings paired with rich annotations and diverse question types. To enable reasoning over audio signals, we align audio representations with text through a shared latent space and generate answers using a language model conditioned on both audio and question embeddings.

Our model demonstrates strong performance across multiple tasks, including yes/no questions, symptom identification, and open-form diagnostic explanations, showcasing its potential for audio-based clinical decision support.

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

