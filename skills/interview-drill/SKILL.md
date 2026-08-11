---
name: interview-drill
description: Rapid-fire coding drills drawn from a question catalogue, tuned to a specific interview.
disable-model-invocation: true
---

A **drill** is repetition in isolation: one pattern, one **rep**, a verdict, next. Breadth over depth — the goal is that no pattern in the pool is unfamiliar on the day, not that any one is mastered.

Setup derives the pool from the user's actual interview. Then the drill runs until they stop it.

## Setup

### 1. Take the brief

Ask for all three at once — these are inputs, not decisions:

- **The interview.** Role, company, format, and any materials they hold: the invitation email, job description, recruiter notes, prior research. The evaluation criteria live here.
- **The source.** Where questions come from: a catalogue URL, a topic list, a repo, a book.
- **The stack.** Language, framework, test runner, and any library that displaces a common default.

_Done when:_ the evaluation criteria are written down in the user's own words where they supplied materials, and inferred and stated back for confirmation where they did not.

### 2. Read the source

Fetch it. Establish every candidate item's name, link, difficulty label if the source carries one, and what it exercises. Verify any library in the stack whose API you would otherwise write from memory — a drill that trains the wrong API is worse than no drill.

_Done when:_ every item the pool might draw from is accounted for, and no fact about the source or the stack rests on recall.

### 3. Cut the pool

Keep items touching three or more of the evaluation criteria. A catalogue's own difficulty label ranks difficulty, not relevance — a hard item exercising one criterion earns less than an easy item exercising four.

Then add outliers on purpose:

- Items matching the company's **domain**, whatever their difficulty — the likeliest seed for a task described as reflecting day-to-day work.
- High-value patterns **absent** from the catalogue, built from scratch.

State inclusions, exclusions, and outliers with the reasoning. The user may move items either way.

_Done when:_ every catalogue item sits in the pool or in the named exclusions.

### 4. Set the mix and the miss-list

Weight **rep** types toward the criteria, so the axis most likely to be dropped under time pressure is the one most drilled. Name the split in percentages.

Write the **miss-list**: the specific errors this stack and these criteria make likely — the ones a verdict watches for. Derive it from the stack, not from a generic idea of good code.

_Done when:_ the split is stated and the miss-list names concrete errors in this stack's idiom.

### 5. Confirm

State back: pool size, mix, controls, and the bar. Then wait. The drill starts on the user's word.

## The drill

One question, one **rep**, one verdict, next.

**Draw** without replacement until the pool empties, then reshuffle. This is what makes breadth real — favourites cluster otherwise.

**Spec in hand.** Before drawing, fetch the task and read its requirements. Where the fetch returns a title or a summary rather than the spec — paywalled, JS-rendered, dead link — ask the user to paste the task text, and wait for it.

_Done when:_ the requirements of the task being drawn from are in context, read rather than assumed.

A rep built from a catalogue blurb invents details the task doesn't have, and the user spends the rep arguing with a fiction instead of writing code.

**One rep, one artifact.** A function, a hook, a type, one state declaration, one callback, one element's JSX, one test. "The state for the checked items" is a rep; "the state and handlers for the component" is three reps wearing one coat, and it lets a wrong answer look reasonable because the scope was never pinned. Where the answer would run past a small code block, narrow it further and draw the rest as separate reps.

Each rep carries the link and names the artifact in a single line. The criterion it targets stays unnamed — naming it gives away the answer, and the interview will not name it either.

**Each rep** is code. A description of code in prose goes back for the code itself; the reflex being built is typing it.

**The bar** is interview-grade, not production-grade. Judge the state shape, the data flow, the naming, the edge case reached or missed, the criteria-specific attribute present or absent. Imports, boilerplate, informal markup, elided sections, and styling all pass without comment. A suboptimal choice carrying a comment that names the better one is a **complete** answer — that is the behaviour the interview rewards.

**Each verdict** runs three or four lines in the interviewer's voice, names the miss, and hands straight to the next question. Where an answer is wrong in a way that would cost the offer, say so plainly.

## Controls

- `skip` — answer given in three lines, next rep. Counts toward the tally: a pattern that would have frozen them is exactly what the debrief needs.
- `more` — full explanation and working code for that one rep.
- `again` — redraw, same task or a different one.

## Checkpoints and debrief

Every ten reps, two lines: which criteria are clean, which recur.

On stop, the debrief — the three weakest patterns ranked, each with its fix. This is the artifact the user carries into the interview, so it names patterns, not individual reps.
