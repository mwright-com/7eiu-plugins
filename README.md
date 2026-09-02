# mwright-book

Tools that come with *7 Elemental, Immutable, Universal Truths: for Building What People
Want with AI*, by Maurice Wright.

[book.mwright.com](https://book.mwright.com)

---

## Install

```
/plugin marketplace add mwrightinc/7eiu-plugins
/plugin install 7eiu-assessment
```

In Cowork, the same thing without a terminal: **Customize → Plugins → + → Add from a
repository**, then install from the list.

---

## What's here

### 7eiu-assessment

An agentic team that reads your business through the seven laws and hands you back a
written assessment.

It runs a guided interview about how your company actually works. Then one agent takes
each chapter and reports what it found under that law: what is already working, where the
opening is, and what you could start on this month. A last agent pulls the seven together
and writes the document.

You get two things. A two-page Quick Read you can hand to anyone, and a full assessment of
eight to ten pages.

Eleven skills: an orchestrator, one per law, a scoring rubric that gates the output, and
two voice skills. Full documentation in
[`plugins/7eiu-assessment/USAGE.md`](plugins/7eiu-assessment/USAGE.md).

Twenty minutes of conversation gets the Quick Read. About an hour gets the full
assessment.

---

## Using it

Ask in plain words:

```
Run my business through the seven principles.

Assess my company using the 7EIU framework and give me the full write-up.

Just the quick read, I have twenty minutes.
```

Or work one law on its own:

```
Principle 4 only. Where is my marketing one-sided?
```

---

## How it stays honest

Three rules, and the scoring skill enforces all three.

**Nothing gets claimed that you did not say.** Every fact traces back to the interview, a
file you supplied, or something the assessor saw. Where the interview did not reach, the
document says so and hands the questions back to you rather than filling the hole with a
plausible guess.

**No tool names, ever.** The document says what a capability does, never what it is
called. Products change every few months. The seven laws do not.

**Nothing ships under 90.** Five dimensions, eight hard fails, and six checks for the
things a business owner notices before they notice a typo: contradictions between
sections, whether the document answered the question you actually asked, whether any
recommendation carrying a real cost says so.

---

© MWRIGHT INC. All rights reserved.
