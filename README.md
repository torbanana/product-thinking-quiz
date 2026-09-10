# Product Thinking Trainer

An interactive, self-paced trainer for the **Product Thinking** learning pathway — learn each
module from a short brief, practise with multiple-choice questions that explain every answer,
then unlock a final scenario quiz.

**▶ [Play it here](https://torbanana.github.io/product-thinking-quiz/)**

## How it works

Each of the seven modules runs in two stages, so nothing is ever asked before it is taught:

1. **Brief** — 4–5 key ideas in plain language, with worked examples.
2. **Practice** — 4–6 multiple-choice questions on what you just read. The explanation appears
   immediately after each answer. Get one wrong and it returns later in the module, so progress
   tracks what you got *correct*, not what you clicked past.

Completing all seven modules unlocks a **final quiz** of 20 applied scenarios — situational
judgement rather than definition-matching, with the answer options shuffled on every attempt.
Results group your misses by module and link straight back to the relevant brief.

Progress and your best quiz score are saved in the browser via `localStorage`.

## Contents

| Module | Topic |
| --- | --- |
| 1 | Understanding the Problem — problems before solutions, outcomes over outputs, Policy-Ops-Tech |
| 2 | Craft a Clear Problem Statement — the 4Cs: Clarity, Consequence, Cause, Confirmation |
| 3 | Start With The Whys — root cause analysis |
| 4 | Metrics — outcome metrics, vanity metrics, guardrails |
| 5 | Assumptions and Risks — surface, stress-test, de-risk |
| 6 | A Good Customer Experience |
| 7 | Key Takeaways |

**55 multiple-choice questions** in total (35 practice + 20 quiz), each with a written explanation.

## Running locally

No build step and no dependencies — it is a single HTML file.

```bash
git clone https://github.com/torbanana/product-thinking-quiz.git
cd product-thinking-quiz
# then just open index.html in a browser
```

## Editing the content

All questions and briefs live in two arrays at the top of the `<script>` block in `index.html`:

- `MODULES` — module titles, briefs (`points`) and practice questions (`practice`)
- `QUIZ` — the final scenario questions

Each question is `{ q, opts, correct, why }`, where `correct` is the index of the right answer in
`opts` and `why` is the explanation shown afterwards. Options are shuffled at runtime, so the
authored order does not matter.

## Attribution

The module titles and themes follow the [Institute of Digital Government's Product Thinking
pathway](https://www.idg.gov.sg/product-thinking/). The briefs, practice questions and quiz
scenarios in this trainer were written for it and are **not** verbatim IDG course material.
