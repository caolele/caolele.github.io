---
layout: post
title: "ICML 2026 in Seoul: Three Works on Game World Modeling and AI-Assisted Peer Review"
date: 2026-07-10 10:00:00-0000
inline: false
related_posts: false
---

Three of my works were presented at [ICML 2026](https://icml.cc/) in Seoul (COEX Convention Center, July 6–11), spanning two themes I care deeply about: **measuring the difficulty of game world modeling** and **making AI a verification layer for peer review**. I joined the conference virtually, with my wonderful co-authors presenting on site.

## Position Track: Profiling Game Worlds by Transition Complexity

My solo position paper argues that game world modeling (GWM) and reinforcement learning research rarely quantify how hard the underlying transition prediction problem actually is. The **Transition Complexity Profile (TCP)** adds the missing denominator: a small, reproducible set of metrics — branching, interaction, and dependency span — that characterizes an environment's induced transition kernel at the declared interface.

<div class="row mt-3 mb-4">
    <div class="col-sm mt-3 mt-md-0">
        <img src="/assets/img/news/20260710-1.png" class="img-fluid rounded z-depth-1" alt="ICML 2026 poster: Position: Profiling Game Worlds by Transition Complexity">
    </div>
</div>

**Measure the world, then compare the model.** Return, rollouts, and loss are useful — but they rarely say how hard the transition problem was.

- 📄 [Paper](https://cspaper.org/openprint/20260514.0002v1) ([arXiv](https://arxiv.org/abs/2608.18079))
- 🎬 [Talk video](https://icml.cc/virtual/2026/poster/67074)
- 🖥️ [Slides](https://icml.cc/media/icml-2026/Slides/67074.pdf)
- 🖼️ [Poster](/assets/img/news/20260710-1.png)

## AI4Science Workshop: AI Should Strengthen Peer Review — Not Imitate or Replace It

At the [AI for Science workshop](https://icml.cc/virtual/2026/workshop/54099), we presented three papers on a shared thesis: AI should augment scientific reasoning and verification — not replace human judgment. The workshop posters were presented on site by my co-authors.

- **[Adopt Machine-Human Collaboration Peer-Review through Computational Research Assessment](https://icml.cc/virtual/2026/73570)** — AI surfaces evidence, disagreement, and reproducibility risks, while humans retain scientific judgment. We propose Computational Research Assessment (CRA) as a discipline-level, method-agnostic agenda: treat disagreement as a signal that triggers escalation instead of averaging; make every critique evidence-linked, reproducible, and contestable; and build a community immune system against gaming and bias.

- **[Preventing the Collapse of Peer Review Requires Verification-First AI](https://icml.cc/virtual/2026/73470)** — Optimize for auditable checks and *truth-coupling* rather than reviewer mimicry or score prediction. We formalize the forces that drive evaluation toward proxy optimization, and argue for deploying AI as an adversarial auditor that expands effective verification bandwidth. ([OpenReview](https://openreview.net/forum?id=oRBjSQFDva), [arXiv](https://arxiv.org/abs/2601.16909))

- **[Position: AI Should Verify, Not Judge, Scientific Work](https://icml.cc/virtual/2026/73440)** (selected as an **oral**) — AI review tools should be utilized primarily by authors during manuscript preparation to verify claims and improve submission quality, grounded in the values of peer review and the scientific process. A collaboration with colleagues from DTU, Oxford, University of Washington, TU Eindhoven, University of Florida, INRIA, University of Copenhagen, and Scholar7.

<div class="row mt-3 mb-4">
    <div class="col-sm mt-3 mt-md-0">
        <img src="/assets/img/news/20260710-2.png" class="img-fluid rounded z-depth-1" alt="ICML 2026 AI4Science Workshop: AI should strengthen peer review, not imitate or replace it">
    </div>
</div>

---

These works reflect an evolution at [CSPaper (Scholar7)](https://cspaper.org): from AI-generated review toward a **verification layer for research** — checking claims, evidence, code, references, and correctness before decisions are made. Grateful to all my collaborators who made these works possible and presented them in Seoul!
