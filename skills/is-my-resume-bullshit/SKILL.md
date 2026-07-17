---
name: is-my-resume-bullshit
description: Audit a resume for its bullshit factor — unsubstantiated claims, causal overclaims, impact-padding — and return a prioritized list of concrete fixes. Use when the user hands over a resume and wants it pressure-tested against a skeptical reader.
---

The one test every line must pass: does it survive **"tell me more about that"** from a skeptical senior engineer across an interview table? A line is **defensible** when it leads with evidence the skeptic can check — a sourced number, a named architecture, a specific problem. It's **bullshit** when it's impact-shaped language with nothing behind it. The job is to find every line that fails the probe and hand back a fix for each.

This is not a scanner. Resume-scoring tools reward the *presence* of impact-shaped language, not whether the impact is real — they routinely score the more dishonest resume higher. Optimize for the skeptic, never for the score.

## Process

1. Read the whole resume once. Then work **bullet by bullet** — every bullet, every summary line, every skills claim. Skimming defeats the skill; the value is catching the line the writer stopped seeing.
2. Run each line against the detectors below. A line can trip more than one.
3. Classify each flagged line by severity (ordering below).
4. Emit the actionable list per the output contract. Done only when every bullet is accounted for and every flagged line carries a concrete rewrite or an explicit cut — never a vague "consider strengthening."

## Detectors

Severity runs high → low; a fabricated or causal claim fails the interview hardest.

**Fabricated / unsourceable metric** *(highest)* — a number with no dashboard, billing console, or record behind it: "10k+ users," "hundreds of manuscripts daily," "thousands of postings." The tell: you couldn't produce the source if asked. Fix: replace with a number you *can* source ("$X MRR at time of departure," "~N monthly reads from the console"), or cut the number and describe the work. A soft number kept is worse than no number.

**Causal overclaim** *(highest)* — crediting your work with a business outcome you can only correlate with: "increased conversion 1.5×," "cut cancellations 15%," "grew organic traffic 20%." The tell: the outcome can't be isolated to you. Fix: assert only what's *directly* yours (an infra cost reduction is; revenue usually isn't), and frame the rest *temporally* — "in the five months after it shipped, X went A → B" — never causally.

**Unmeasured impact claim** — an outcome asserted but never measured: "significantly reduced regressions," "improved performance," "improved reliability by expanding test coverage." The tell: a claimed metric standing as its own evidence. Fix: state what you *did* (grew coverage, made the codebase agent-ready) and drop the outcome you never measured.

**Impact-padding (the X-Y-Z reflex)** — a factual bullet with a bolted-on outcome clause: "shipped the canvas primitives, *enabling richer diagramming*"; "*supporting* team velocity"; "*expanding* the platform's capabilities." The tell: the clause after the comma says nothing checkable. This is the signature of AI-written resumes and of every resume-improver tool. Fix: cut the clause. The fact stands on its own.

**Domain overclaim** — inflating a technical task into domain expertise: a Stripe integration framed as "fintech experience." The tell: the skill is real, the domain claim isn't. Fix: claim the skill (payment integration), not the domain.

**Weak-verb hedge** — "contributed to," "helped with," "supported," "was involved in." The tell: vague *and* it undersells what's actually yours. Fix: a precise, defensible strong verb — Architected, Drove, Engineered — but only where accurate. The fix is precision, not a swing into causal overclaim.

**Vague scale / marketing** — "production-grade at scale," "highly performant," round-number flexes like "handles 10,000 docs." The tell: conditions and limits are missing. Fix: state the *conditions*, report the *measured* number, and *name the limit* — "p95 <100ms through ~800 concurrent docs on a 4GB node; memory-bound past that." Naming your own ceiling reads as engineering; a bare round number reads as marketing.

**Informal filler / non-signal** *(lowest)* — "helping users overcome blank-page syndrome," a lone "mentored a junior dev" standing in for a whole leadership story, a bullet with no signal in it. The tell: it occupies a line without earning it. Fix: replace with a technically specific account of what was built, or cut.

**Missing "why it mattered"** — the inverse failure: a bullet states *what* but not why it was hard, so the signal is invisible to the reader. Fix: add *truthful* difficulty context ("most tracked-changes implementations flatten these edits") — never invented impact. Use sparingly; it competes with brevity.

## Guardrails — don't reintroduce bullshit while fixing

- Never append an outcome clause to "strengthen" a bullet. That is the impact-padding detector run in reverse, and it's the most common way a rewrite smuggles bullshit back in.
- Don't manufacture a metric to fill a gap. "Quantify where you can" holds only where the number is real; no defensible number → describe the work.
- Don't chase scanner scores or stuff keywords. The single scanner signal worth heeding is repeated-verb detection; the rest is priced in invented data.
- Don't bolt a target-role phrase onto the summary. The reader already knows the role they're hiring for.
- Falsifiable and slightly rough beats polished. Over-editing reads as generated; specificity is the credibility signal.

Prose-level AI tells — em-dash overuse, trailing -ing phrases, filler hyphen-pairs like "end-to-end," rule-of-three — are a different axis. Route those to the **humanizer** skill rather than handling them here.

## Output contract

Return one prioritized list, highest-severity first. Each item:

- the offending line, quoted verbatim;
- the detector that fired, in a phrase;
- the fix — a concrete rewrite *or* an explicit cut. Never "consider revising."

Close with the single line that matters: which bullets, if any, still wouldn't survive "tell me more about that."
