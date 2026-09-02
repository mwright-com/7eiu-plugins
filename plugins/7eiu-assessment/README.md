# The 7EIU Assessment Team

An agentic team that reads your business through the seven laws in *7 Elemental,
Immutable, Universal Truths*, and hands you back a written assessment.

It runs a guided interview about how your company actually works. Then one agent takes
each chapter and reports what it found under that law: what is already working, where the
opening is, and what you could start on this month. A last agent pulls the seven together
and writes the document.

You get two things. A two-page Quick Read you can hand to anyone, and a full assessment
of eight to twelve pages built the way the reference engagement was built.

---

## Installing it

```
/plugin marketplace add mwright-book
/plugin install 7eiu-assessment
```

Or drop the `skills/` folders into your skills directory if you would rather not use the
plugin.

---

## Running it

Say what you want:

> Run my business through the seven principles.

> Assess my company using the 7EIU framework and give me the full write-up.

> Just the quick read, I have twenty minutes.

The orchestrator takes it from there. Expect an interview: about twenty minutes for the
Quick Read, about an hour for the full assessment. Bring anything you have. Your site, a
deck, a price list, past proposals, notes.

To work one law on its own, ask for it:

> Principle 4 only. Where is my marketing one-sided?

---

## What is in the box

| Skill | What it does |
|---|---|
| `7eiu-assessment-orchestrator` | Runs the engagement. Interview, dispatch, assembly, the gate. |
| `7eiu-law-1-intention-and-action` | Leadership. What you actually want, and whether anyone downstream can tell. |
| `7eiu-law-2-big-and-small` | Process. Which large-company patterns you could shrink, and which of your instincts to protect. |
| `7eiu-law-3-being-consistent` | Operations. The note you hold, and what breaks it. |
| `7eiu-law-4-active-and-passive-marketing` | Marketing. Reach, magnetism, and the marketing garden. |
| `7eiu-law-5-wins-and-losses` | Support. Whether anything gets learned from how customers go. |
| `7eiu-law-6-rhythm-and-fit` | Relations. Where you sit against a market that keeps moving. |
| `7eiu-law-7-karma-and-value` | Evaluation, and the closing synthesis. |
| `7eiu-principle-fidelity-scorer` | The gate. Scores the draft 0 to 100. Nothing ships under 90. |
| `7eiu-mo-voice` | Maurice Wright's voice, calibrated for assessment writing. |
| `7eiu-human-voice` | Strips the tells that make writing read as machine-written. |

---

## How it keeps itself honest

Three rules do most of the work.

**Nothing gets claimed that you did not say.** Every fact in the finished document traces
back to the interview, a file you supplied, or something the assessor saw. Inference does
not get promoted to observation.

**The holes stay visible.** Where the interview did not reach, the document says so and
hands the questions back to you, in italics, for you to answer. That is how the reference
document handled it, and it is the reason the rest of it can be trusted.

**No tool names, ever.** The document says what a capability does, never what it is
called. Products change every few months. The seven laws do not. An assessment that names
this year's software is out of date before you have acted on it.

The scorer enforces all three, plus voice and structure, and refuses to pass a draft that
breaks one.

---

## Extending it

`skills/7eiu-assessment-orchestrator/references/chapter_skill_contract.md` documents the
interface every chapter skill honors. Build a new one to that contract and the
orchestrator will pick it up without changes.

`references/benchmark_spec.md` is the document target. It settles most arguments about
shape and tone.

The MWRIGHT INC mark is packaged at
`skills/7eiu-assessment-orchestrator/assets/mark.png` and renders on every page. Drop a
different `mark.png` beside an assessment to run it under another brand.

---

*7 Elemental, Immutable, Universal Truths: for Building What People Want with AI*
Maurice Wright · [book.mwright.com](https://book.mwright.com)
