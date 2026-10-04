---
layout: post
title: "The Improvement Loop: Talks on Self-Improving Agents at Proxify, Kunumi Institute, and DanAds"
date: 2026-10-02 10:00:00-0000
inline: false
related_posts: false
---

<style>
.rsi-eyebrow {
    font-size: 0.78rem;
    font-weight: 700;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: #3aa28f;
    margin-bottom: 0.25rem;
}
.rsi-venues {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(190px, 1fr));
    gap: 14px;
    margin: 1.5rem 0 2rem;
}
.rsi-venue {
    border: 1px solid var(--global-divider-color);
    border-left: 4px solid #3aa28f;
    border-radius: 0.4rem;
    padding: 0.9rem 1rem;
}
.rsi-venue h4 {
    font-size: 1.05rem;
    margin: 0 0 0.3rem;
}
.rsi-venue p {
    font-size: 0.88rem;
    margin: 0;
    line-height: 1.45;
}
.rsi-stat {
    font-size: 1.9rem;
    font-weight: 700;
    color: #3aa28f;
    line-height: 1.1;
}
.rsi-acts .caption {
    font-size: 0.82rem;
}
article h2 {
    margin-top: 2.2rem;
}
.rsi-pull {
    border-left: 4px solid #3aa28f;
    padding: 0.2rem 0 0.2rem 1rem;
    font-size: 1.15rem;
    font-style: italic;
}
</style>

<div class="row mt-3 mb-2">
    <div class="col-sm">
        <a href="https://drive.google.com/file/d/1kCoV4lWkHK3VDaVOR0p6Ls2y4SumosIc"><img src="/assets/img/news/20261002-cover-1600.webp" srcset="/assets/img/news/20261002-cover-800.webp 800w, /assets/img/news/20261002-cover-1600.webp 1600w" sizes="(min-width: 992px) 800px, 100vw" width="1600" height="900" loading="eager" decoding="async" class="img-fluid rounded z-depth-1" alt="Title slide: The Improvement Loop, Self-Improving Agents, Fundamentals and Use Cases"></a>
        <div class="caption">The title slide from the Kunumi Institute edition of the deck. The core material stayed the same across all three sessions.</div>
    </div>
</div>

**What happens when an AI system starts improving the way it improves itself?** That question, recursive self-improvement (RSI), took me to three very different audiences this autumn. The talk was well received, so it ended up traveling.

<div class="rsi-venues">
    <div class="rsi-venue">
        <div class="rsi-eyebrow">Stockholm · Sep 22</div>
        <h4><a href="https://luma.com/jr9gwcr7">Proxify Talks</a></h4>
        <p>A breakfast keynote: <em>Self-Improving Agents: From Prompt Engineering to Hyperagents</em>.</p>
    </div>
    <div class="rsi-venue">
        <div class="rsi-eyebrow">Research · Oct 2</div>
        <h4><a href="https://www.kunuminst.org/en">Kunumi Institute</a></h4>
        <p>Invited by Dhiana Deva for <em>a conversation with</em> the research collective.</p>
    </div>
    <div class="rsi-venue">
        <div class="rsi-eyebrow">Industry · Oct 16</div>
        <h4><a href="https://danads.com/">DanAds</a></h4>
        <p>Invited by Reza Malekzadgan to speak at the global ad-tech company.</p>
    </div>
</div>

Each session drew **60–100 people**, a clear sign of how many engineers, researchers, and business leaders are thinking about this topic right now.

<div class="row mt-3">
    <div class="col-sm">
        <img src="/assets/img/news/20261002-6-1600.webp" srcset="/assets/img/news/20261002-6-800.webp 800w, /assets/img/news/20261002-6-1600.webp 1600w" sizes="(min-width: 992px) 800px, 100vw" width="1600" height="1066" loading="lazy" decoding="async" class="img-fluid rounded z-depth-1" alt="A full room at Proxify in Stockholm during the talk">
        <div class="caption">A full room at Proxify in Stockholm, here during the game-testing section.</div>
    </div>
</div>

## Opening with a provocation

<div class="row mt-3 align-items-center">
    <div class="col-md-6 mb-3 mb-md-0">
        <img src="/assets/img/news/20261002-1-1600.webp" srcset="/assets/img/news/20261002-1-800.webp 800w, /assets/img/news/20261002-1-1600.webp 1600w" sizes="(min-width: 768px) 400px, 100vw" width="1600" height="1066" loading="lazy" decoding="async" class="img-fluid rounded z-depth-1" alt="Lele Cao opening the talk with the slide: Google DeepMind has solved RSI?">
    </div>
    <div class="col-md-6">
        <p>I opened with a question: <em>has Google DeepMind solved RSI?</em> Headlines and rumors say "AI improves AI" is already here, from <a href="https://deepmind.google/blog/alphaevolve-a-gemini-powered-coding-agent-for-designing-advanced-algorithms">AlphaEvolve</a> speeding up Gemini training kernels to <a href="https://arxiv.org/html/2607.07663v1">a sharp rise in RSI papers</a>. But a rising paper count measures research activity, not demonstrated recursive capability. The rest of the talk was about telling the two apart.</p>
    </div>
</div>

## 01 · Understanding RSI

The key question is **who makes the next version**. Engineers shipping releases is ordinary progress. The recursive step comes when the system proposes and tests edits it can retain, and eventually improves *how* the next improvement is produced. I walked through seven levels of self-improvement: from a better answer, to a better agent, to improving the improver, to developing a successor model. I mapped representative systems onto them, including Karpathy's [autoresearch](https://github.com/karpathy/autoresearch), Meta's [HyperAgents](https://ai.meta.com/research/publications/hyperagents/), [MetaRSI](https://arxiv.org/abs/2609.06396), and Google's [RRSI](https://arxiv.org/abs/2609.24972).

<div class="row mt-3">
    <div class="col-md-6 mb-3 mb-md-0">
        <img src="/assets/img/news/20261002-3-1600.webp" srcset="/assets/img/news/20261002-3-800.webp 800w, /assets/img/news/20261002-3-1600.webp 1600w" sizes="(min-width: 768px) 400px, 100vw" width="1600" height="1066" loading="lazy" decoding="async" class="img-fluid rounded z-depth-1" alt="Explaining how Karpathy's autoresearch makes the improvement loop concrete">
    </div>
    <div class="col-md-6">
        <img src="/assets/img/news/20261002-4-1600.webp" srcset="/assets/img/news/20261002-4-800.webp 800w, /assets/img/news/20261002-4-1600.webp 1600w" sizes="(min-width: 768px) 400px, 100vw" width="1600" height="1067" loading="lazy" decoding="async" class="img-fluid rounded z-depth-1" alt="Audience photographing the seven levels of self-improvement slide">
    </div>
</div>
<div class="caption">Left: autoresearch as a concrete edit, train, measure, keep-or-revert loop. Right: phones up for the "seven levels" slide.</div>

<div class="row mt-4 align-items-center">
    <div class="col-md-5 mb-3 mb-md-0">
        <img src="/assets/img/news/20261002-5-1600.webp" srcset="/assets/img/news/20261002-5-800.webp 800w, /assets/img/news/20261002-5-1600.webp 1600w" sizes="(min-width: 768px) 330px, 100vw" width="1600" height="1066" loading="lazy" decoding="async" class="img-fluid rounded z-depth-1" alt="Lele Cao explaining the universal improvement loop">
    </div>
    <div class="col-md-7">
        <p class="rsi-pull">Keep tests and scoring rules outside the candidate's edit permissions.</p>
        <p>The universal loop of RSI is simple: run and inspect, propose variants, then evaluate and select against a baseline on fresh tasks at a matched budget. The hard part is the evaluator. If the system can edit the thing that grades it, you no longer have an improvement loop.</p>
    </div>
</div>

## Three use cases

<div class="row mt-3 rsi-acts">
    <div class="col-md-4 mb-3">
        <img src="/assets/img/news/20261002-s2-1600.webp" srcset="/assets/img/news/20261002-s2-800.webp 800w, /assets/img/news/20261002-s2-1600.webp 1600w" sizes="(min-width: 768px) 260px, 100vw" width="1600" height="900" loading="lazy" decoding="async" class="img-fluid rounded z-depth-1" alt="Section 02: RSI in Game Testing">
        <div class="caption"><strong>02 · Game testing.</strong> Jiayi Weng's coding agents rewrite their own controllers on <a href="https://trinkle23897.github.io/learning-beyond-gradients">Atari57</a>. At King, we tested this loop to align heuristic bots' attempts-per-success with human players.</div>
    </div>
    <div class="col-md-4 mb-3">
        <img src="/assets/img/news/20261002-s3-1600.webp" srcset="/assets/img/news/20261002-s3-800.webp 800w, /assets/img/news/20261002-s3-1600.webp 1600w" sizes="(min-width: 768px) 260px, 100vw" width="1600" height="900" loading="lazy" decoding="async" class="img-fluid rounded z-depth-1" alt="Section 03: RSI in Paper Review">
        <div class="caption"><strong>03 · Paper review.</strong> Our <a href="https://cspaper.org/openprint/20260601.0001v1">SIRA</a> agent factory behind <a href="https://cspaper.org">CSPaper</a>, where domain experts regularize what the loop may change.</div>
    </div>
    <div class="col-md-4 mb-3">
        <img src="/assets/img/news/20261002-s4-1600.webp" srcset="/assets/img/news/20261002-s4-800.webp 800w, /assets/img/news/20261002-s4-1600.webp 1600w" sizes="(min-width: 768px) 260px, 100vw" width="1600" height="900" loading="lazy" decoding="async" class="img-fluid rounded z-depth-1" alt="Section 04: RSI for Superconductor Discovery">
        <div class="caption"><strong>04 · Superconductor discovery.</strong> <a href="https://arxiv.org/abs/2604.23758">ElementsClaw</a> pairs atomic models and LLM agents with physical lab feedback.</div>
    </div>
</div>

The paper-review results drew the most questions. Under a matched budget (same base model, evaluator, and number of scored candidates), SIRA's constrained, expert-guided search outperformed a HyperAgents-style open search on best validation decision-label accuracy (agreement with historical accept/reject decisions):

<div class="row text-center my-3">
    <div class="col-6 col-md-3"><div class="rsi-stat">0.941</div><small>SIRA decision-label accuracy (± 0.018)</small></div>
    <div class="col-6 col-md-3"><div class="rsi-stat">0.865</div><small>HyperAgents-style (± 0.049)</small></div>
    <div class="col-6 col-md-3"><div class="rsi-stat">2–5</div><small>candidates to best, vs. 6–15</small></div>
    <div class="col-6 col-md-3"><div class="rsi-stat">0.849</div><small>AUC in our <a href="https://cspaper.org/articles/introducing-review-rank">ICLR in-field test</a></small></div>
</div>

A smaller, better-regularized search space found a stronger candidate sooner. The superconductor case showed the other half of the lesson: a plausible crystal can pass the structure check and still fail the property test. **Credible feedback, whether from experts, production, or the physical lab, is what closes the loop.**

## The rooms

<div class="row mt-3">
    <div class="col-md-6 mb-3 mb-md-0">
        <img src="/assets/img/news/20261002-7-1600.webp" srcset="/assets/img/news/20261002-7-800.webp 800w, /assets/img/news/20261002-7-1600.webp 1600w" sizes="(min-width: 768px) 400px, 100vw" width="1600" height="1066" loading="lazy" decoding="async" class="img-fluid rounded z-depth-1" alt="Audience at Proxify listening to the talk">
    </div>
    <div class="col-md-6">
        <img src="/assets/img/news/20261002-2-1600.webp" srcset="/assets/img/news/20261002-2-800.webp 800w, /assets/img/news/20261002-2-1600.webp 1600w" sizes="(min-width: 768px) 400px, 100vw" width="1600" height="1066" loading="lazy" decoding="async" class="img-fluid rounded z-depth-1" alt="Camera operator filming the talk at Proxify">
    </div>
</div>
<div class="caption">An engaged audience at Proxify, and the crew filming the session.</div>

I closed each session with open questions for practitioners, and they kept the Q&A lively. What change should survive into the next attempt? Where does credible feedback come from? How do you price an accepted outcome? And what is the irreplaceable role of the human?

<div class="row mt-3">
    <div class="col-sm">
        <img src="/assets/img/news/20261002-8-1600.webp" srcset="/assets/img/news/20261002-8-800.webp 800w, /assets/img/news/20261002-8-1600.webp 1600w" sizes="(min-width: 992px) 800px, 100vw" width="1600" height="1067" loading="lazy" decoding="async" class="img-fluid rounded z-depth-1" alt="Closing the Proxify session with the host">
        <div class="caption">Wrapping up at Proxify with the host. Thank you for the warm welcome!</div>
    </div>
</div>

## Resources

- 🖥️ **Slide deck:** [The Improvement Loop: Fundamentals and Use Cases](https://drive.google.com/file/d/1kCoV4lWkHK3VDaVOR0p6Ls2y4SumosIc)
- 📅 **Event page:** [Proxify Talks: Self-Improving Agents](https://luma.com/jr9gwcr7)
- 🧪 **Our work:** [SIRA agent factory](https://cspaper.org/openprint/20260601.0001v1) · [CSPaper Review Rank](https://cspaper.org/articles/introducing-review-rank) · [CSPaper](https://cspaper.org)
- 📚 **Referenced systems:** [autoresearch](https://github.com/karpathy/autoresearch) · [HyperAgents](https://ai.meta.com/research/publications/hyperagents/) · [MetaRSI](https://arxiv.org/abs/2609.06396) · [RRSI](https://arxiv.org/abs/2609.24972) · [AlphaEvolve](https://deepmind.google/blog/alphaevolve-a-gemini-powered-coding-agent-for-designing-advanced-algorithms) · [Learning Beyond Gradients](https://trinkle23897.github.io/learning-beyond-gradients) · [ElementsClaw](https://arxiv.org/abs/2604.23758)

## What's next

Thank you to Proxify, to Dhiana Deva and Kunumi Institute, and to Reza Malekzadgan and the DanAds team for the invitations and the sharp questions. Unfortunately, with my limited bandwidth, I can't accept further talk invitations for now.

My focus now is on applying RSI where it creates real business value and real benefit for people. Foundation models keep getting better every few months, so a well-built improvement loop gets a stronger engine each time the underlying model is upgraded. The lasting advantage lies in what sits around the model: trustworthy evaluators, expert-shaped search spaces, and feedback grounded in the real world. That is the layer I'm building, from game testing at King to research verification at CSPaper. If you're working on loops like these, I'd love to compare notes.
