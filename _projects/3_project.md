---
layout: page
title: "TRIAGE: Adaptive Test-Time Scaling for Zero-Shot Respiratory Audio Classification"
description: "A zero-shot respiratory audio classification framework that adaptively allocates test-time compute to uncertain cases."
img: assets/img/triagefig.png
importance: 2
category: work
related_publications: true
---

This project corresponds to our paper {% cite wang2026adaptivetesttimescaling %}.

TRIAGE (**Tiered Retrieval and Inference for Audio with Gated Escalation**) is a zero-shot respiratory audio classification framework that improves medical audio inference without task-specific training. Instead of applying the same inference procedure to every recording, TRIAGE adaptively routes each sample through progressively richer reasoning stages depending on prediction confidence.

The framework starts with a fast **Tier-L** stage that performs label-cosine scoring in a frozen audio–text embedding space. Confident cases are finalized immediately, while uncertain cases are escalated to **Tier-M**, where clinician-style descriptor templates are matched against the audio and converted into rule-based predictions. The most ambiguous recordings are further routed to **Tier-H**, which retrieves similar audio–report examples and uses an LLM to make an evidence-grounded final decision.

Across **nine respiratory audio classification tasks** spanning cough, exhalation, and lung-sound datasets, TRIAGE achieves strong zero-shot performance, reaching a mean AUROC of **0.744** without any task-specific training. The adaptive router concentrates additional computation where it matters most: high-confidence cases exit early, while uncertain cases benefit from descriptor-based reasoning and retrieval-augmented LLM inference. :contentReference[oaicite:0]{index=0}

<div class="row mt-4">
  <div class="col-sm-12">
    {% include figure.liquid path="assets/img/triagefig.png" title="Overview of the TRIAGE framework." class="img-fluid rounded z-depth-1" %}
  </div>
</div>

<div class="caption">
  TRIAGE performs adaptive test-time scaling for zero-shot respiratory audio classification by routing recordings through label matching, clinical descriptor reasoning, and retrieval-augmented LLM inference.
</div>
