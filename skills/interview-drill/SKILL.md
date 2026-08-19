---
name: interview-drill
description: Rapid-fire drills tuned to one interview — coding, system design, or behavioral.
disable-model-invocation: true
---

A **drill** is repetition in isolation: one **rep**, a verdict, next. Breadth over depth — the goal is that no pattern is unfamiliar on the day, not that any one is mastered.

The loop holds whatever the interview: a question small enough to answer in one block, an answer that is an artifact rather than a description of one, a verdict, the next question. What changes between interview types is the shape of the artifact.

Setup derives the pool from the user's actual interview. Then the drill runs until they stop it.

## Setup

### 1. Take the brief

Ask for all three at once — these are inputs, not decisions:

- **The interview.** Type, role, company, format, and any materials they hold: the invitation email, job description, recruiter notes, prior research. The evaluation criteria live here.
- **The source.** Where reps come from. Three shapes, and it matters which:
  - a **catalogue** — many discrete items, drawn between (a question bank, a problem list)
  - a **topic** — one domain, drawn within (caching, React state, negotiation stories)
  - a **problem** — one artifact, drawn across its facets (design a rate limiter; the promotion you were denied)
- **The stack.** For coding: language, framework, test runner, any library displacing a common default. For system design: scale, constraints, whether a drawing tool is used. For behavioral: the competency list, the format expected.

_Done when:_ the evaluation criteria are written down in the user's own words where they supplied materials, and inferred and stated back for confirmation where they did not.

### 2. Read the source

Fetch it. For a catalogue, establish every candidate item's name, link, and what it exercises. For a topic or a problem, establish its actual boundaries.

Verify anything whose particulars would otherwise come from recall — a library's API, a spec's requirements, a company's published architecture. A drill built on a misremembered API trains the wrong reflex.

_Done when:_ every item the pool might draw from is accounted for, and no fact about the source or the stack rests on memory.

### 3. Cut the pool

Keep what touches three or more of the evaluation criteria. A catalogue's difficulty label ranks difficulty, not relevance — an easy item exercising four criteria earns more than a hard one exercising one. For a topic or a problem, the same cut applies to its facets.

Then add outliers on purpose:

- Whatever matches the company's **domain**, whatever its difficulty — the likeliest seed for a task described as reflecting day-to-day work.
- High-value patterns **absent** from the source, drilled from scratch.

State inclusions, exclusions, and outliers with the reasoning, and move anything the user asks moved.

_Done when:_ everything the source offers sits in the pool or in the named exclusions.

### 4. Set the mix and the miss-list

Weight **rep** types toward the criteria, so the axis most likely to be dropped under pressure is the one most drilled. Name the split in percentages.

Write the **miss-list**: the specific errors this stack and these criteria make likely — the ones a verdict watches for. Derive it from the material, not from a generic idea of good work.

_Done when:_ the split is stated and the miss-list names concrete errors in this domain's idiom.

### 5. Confirm

State back pool size, mix, controls, and the bar. Then wait.

_Done when:_ the user has answered, and the drill starts on their word.

## The drill

**Draw** without replacement until the pool empties, then reshuffle. This is what makes breadth real — favourites cluster otherwise.

**Material in hand.** Before drawing, read what the rep draws on: the task's requirements, the topic's actual scope, the problem's constraints. Where a fetch returns a title or a summary rather than the substance — paywalled, JS-rendered, dead link — ask the user to paste it, and wait.

A rep built from a blurb invents details the material does not have, and the user spends the rep arguing with a fiction instead of working.

_Done when:_ the material behind the rep is in context, read rather than assumed.

**One rep, one artifact.** A rep is **atomic**: it stands alone, and it is one piece of the larger picture rather than a corner of one. Too big and a wrong answer looks reasonable because the scope was never pinned; too small and nothing is exercised. Scoping is the whole craft here.

By interview type, a rep is:

- **Coding** — a function, a hook, a type, one state declaration, one callback, one element's markup, a test.
- **System design** — an API contract, a data model, a named cache strategy with its invalidation, one failure mode and its mitigation, a capacity estimate, the trade-off between two named options.
- **Behavioral** — the situation and task of one story in four sentences, the specific decision inside a story already told, the metric that showed it worked, the version of a failure story that does not flinch.

"The state for the checked items" is atomic; "the state and handlers for the component" is three reps wearing one coat. "Where does the write go" is atomic; "design the system" is the interview. Where an answer would run past one block, narrow it and draw the rest separately.

Each rep names the artifact in a single line, with a link where one exists. The criterion it targets stays unnamed — naming it gives away the answer, and the interview will not name it either.

**Each rep is the artifact.** Prose about what one would write goes back for the thing itself; the reflex being built is producing it.

**The bar** is interview-grade. Judge the shape of the thinking: the structure chosen, the data flow, the naming, the edge case reached or missed, the criteria-specific move present or absent. A suboptimal choice carrying a comment that names the better one is a **complete** answer — that is the behaviour the interview rewards.

Grade what an editor could not have caught. A chat box has no autocomplete and no type checker, so a mistyped identifier or a mismatched pair is an artifact of the medium, and calling it a finding buries the real ones. What survives the discount is anything tooling would also miss: a name that typechecks but points at the wrong thing, a missing `await` on something returning a promise, a plausible value that is simply wrong.

**Each verdict** runs three or four lines in the interviewer's voice, names the miss, and hands straight to the next rep. Where an answer is wrong in a way that would cost the offer, say so plainly.

Trace the failure before asserting one: follow the answer through the case that supposedly breaks it and confirm it breaks. An overcalled bug costs a rep in argument and spends credibility the real findings need. Where something is a smell rather than a defect, say which.

## Controls

- `skip` — answer given in three lines, next rep. Counts toward the tally: a pattern that would have frozen them is exactly what the debrief needs.
- `more` — full explanation and working artifact for that one rep.
- `again` — redraw.

## When the pool is wrong

The pool is a bet on what the interview will ask, and bets lose. When the user reports that the real thing fell outside it, or asks for something the cut excluded, add it and say what the miss implies — a whole region of the source went undrilled, and knowing that beats defending the cut.

## Checkpoints and debrief

Every ten reps, two lines: which criteria are clean, which recur.

On stop, the debrief — the three weakest patterns ranked, each with its fix. This is the artifact the user carries into the interview, so it names patterns, not individual reps.
