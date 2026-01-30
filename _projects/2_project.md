---
layout: page
title: "AcuLa: Language Models as Semantic Teachers"
description: "A lightweight post-training audio–language alignment framework that injects clinical semantics into medical audio encoders."
img: assets/img/aculafig.png
importance: 2
category: work
related_publications: true
---

This project corresponds to our paper {% cite wang2025semanticteachers %}.

AcuLa (Audio–Clinical Understanding via Language Alignment) is a lightweight post-training framework that turns “acoustically strong but semantically blind” medical audio encoders into clinically-aware representations by aligning them with a frozen medical language model acting as a **semantic teacher**. :contentReference[oaicite:0]{index=0}

To scale audio–text pairing, we generate large-scale clinical reports from structured metadata using off-the-shelf LLMs, then align audio and text representations with a **CKA-based representation alignment loss** while preserving fine-grained acoustic cues via an additional self-supervised objective. We evaluate across **18 cardio-respiratory tasks** and observe strong gains (e.g., mean AUROC improvements and large boosts on challenging cough-based diagnosis). :contentReference[oaicite:1]{index=1}

<div class="row mt-4">
  <div class="col-sm-12">
    {% include figure.liquid path="assets/img/aculafig.png" title="Overview of the AcuLa framework." class="img-fluid rounded z-depth-1" %}
  </div>
</div>

<div class="caption">
  AcuLa aligns medical audio encoder representations with language representations from a frozen medical LLM (semantic teacher), while retaining acoustic detail via a self-supervised objective. :contentReference[oaicite:2]{index=2}
</div>
