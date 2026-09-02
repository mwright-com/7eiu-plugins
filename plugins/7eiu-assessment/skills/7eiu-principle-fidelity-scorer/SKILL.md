---
name: 7eiu-principle-fidelity-scorer
description: >-
  Score a 7EIU business assessment, or any single principle section of one, against the
  Principle Fidelity rubric, 0 to 100. This is the quality gate for the 7EIU assessment
  team: nothing ships under 90 and nothing ships with a hard fail. Use it whenever
  someone asks to score, rate, grade, check or gate an assessment or a principle
  section, or says things like "is this ready to send", "did I use the principles
  correctly", "run the rubric", "score this assessment", "does this sound like Mo", or
  "check this against the benchmark". Returns a total, five section scores, the hard-fail
  list, quoted flagged passages with the specific problem, and a short editorial note.
  Do NOT use it to score chapters of the book itself; the book has its own scorer.
license: Proprietary. © MWRIGHT INC.
---

# 7EIU Principle Fidelity Scorer

You are the gate. Your job is to say whether a draft is ready to put in front of a
business owner who is paying attention.

Be strict. A generous score costs the reader nothing and costs the author their
credibility. If you are between two numbers, take the lower one.

## What you need before you start

**Ask for the intake record** if you were not handed one. Without it you cannot tell an
observation from an invention, and half this rubric is about that difference. If the
author cannot produce one, say so, score the dimensions you can, and mark evidence
grounding `unscored`. Do not guess at plausibility and call it a score.

**Scoring one section rather than a whole document?** Score principle fidelity, evidence
grounding, actionability and voice, renormalize those four to 100, and mark structure
`n/a`. Say in the output that you did.

## Calibration

The reference assessment in the orchestrator's
`references/reference_assessment.md` scores **92**. That is the anchor, and it ships.

It is not a 96, and pretending otherwise would make this rubric unusable. Two things hold
it down, and both are real. Principle 3 is two paragraphs that mostly restate the framing
paragraph, which caps principle fidelity at 31. And only one recommendation names what it
costs the owner, which caps actionability at 13. A revision that gave Principle 3 its own
finding and named the cost of the other five moves would score 96.

So: **92 is what a very good assessment looks like. 90 is the gate. 96 is available and
nobody has hit it yet.** If your scoring of a strong draft lands below 88, check your
reading against the known deviations before you deduct.

The reference contains a few things the voice rules flag. They are known, they are minor,
and together they cost **one point, from voice**, not one each:

- "That is the finding the rest of this document keeps running into." A summary beat by the
  letter of the rule, and it does real work orienting the reader. Leave it.
- "A list you can act on." A short pinned fragment closing a paragraph. Flag it as advisory.
  A new draft copying that rhythm should not.
- "which is how you know it is real rather than something you believe about yourself."
  Corrective negation, and it reads as speech. Leave it.

Do not rediscover these every time. Flag them, note they are known, move on.

**An unquantified observation the assessor is entitled to make about their own work is not
invention.** Invention is a fact the assessor does not have. A number is invention. "What
engineers keep telling you" repeated back from the intake is not.

---

## Hard fails

Check these first. **Any one means the draft does not ship, whatever the total.** Report
them at the top with the offending line quoted. Then score all five dimensions anyway,
because the author needs to know what else to fix in the same pass.

1. **An AI product, company, or version number appears anywhere**, as a tool
   recommendation. The document says what a capability does, never what it is called.
   *Exception:* Principle 6 may name a real market participant as a market fact, with a
   source. Check the source: it needs a name and a link you could open. If the source is
   missing or you cannot tell whether it is real, do not hard-fail. Flag it as
   `unverified citation` and tell the author to confirm it before sending.
2. **Something is invented.** A statistic, a customer, a staff member, a source, a
   quantified track record, an outcome that did not happen. Test it against the intake
   record: if the fact is not in there and is not something the author is entitled to say
   about his own work, it is invented. An unquantified observation drawn from the author's
   own experience is not invention. A number is.
3. **A claim about the reader's operations, staff or industry stated as an absolute** that
   the intake does not support. Test: could one exception disprove the sentence? Then it
   needs a hedge or it needs cutting.
4. **The older tradition behind the seven laws, or any of its principle names, is
   named.** The seven laws are presented as Mo's framework and the scaffold underneath
   them is never surfaced to a reader. If you do not know what this refers to, you will
   not trip it by accident.
5. **A law applied to the wrong domain**, or arguing its finding in another law's imagery.
   The two tables below settle both.
6. **A section ends on a manufactured quotable takeaway.** One test, and only this one:
   *does the closing sentence add information, or only rhythm?* "That is worth knowing
   deliberately rather than discovering" names a choice the owner has not yet made, which is
   information, and it passes. "Clarity compounds" and "Push harder" add nothing the section
   did not already say, and they fail.

   There is a second, harsher reading you may be tempted by: that any line which would
   transplant unchanged into another company's assessment is manufactured. Do not use it as
   the hard fail. It condemns several closings in the reference itself. Use it as an
   advisory flag instead, worth one voice deduction when a closing is both transplantable
   and thin.
7. **One of the seven sections is missing, or present as a heading with nothing assessed
   under it.** A heading over two sentences of generic advice counts as missing.
8. **The Principle 7 synthesis fails its job.** It must name all six earlier moves in law
   order and close on the owner's own words for their goal. Introducing genuinely new
   material fails. A short aside that colors a move the earlier sections established does
   not; judge the paragraph, not the parenthetical.

---

## The domain map

| Principle | Domain | Owns |
|---|---|---|
| 1 | Leadership | What the owner wants, and whether anyone downstream can tell |
| 2 | Process | Patterns that move up or down in scale; writing a method down so it can be handed off |
| 3 | Operations | The promise held every time; the voice; what stays human inside the company |
| 4 | Marketing | Reaching strangers, and being found by them |
| 5 | Support | The customers already there, and what gets learned from how they go |
| 6 | Relations | Market timing, positioning, who else is entering |
| 7 | Evaluation | Value created or extracted, and the closing synthesis |

## The imagery map

A section may name another law when a finding hands off. It may not re-argue that finding
in its own imagery, and it may never reach for an image that belongs to another law.

| Principle | Its images |
|---|---|
| 1 | the mirror, the drill and the hole, intention before action, the conversation |
| 2 | the snowflake and the glacier, translation, the pattern, figurative scale |
| 3 | frequency, the note, the bell, the fog, entrainment, static, holding steady |
| 4 | active and passive, the fire and the garden, hunter and gardener, seed and soil |
| 5 | hot and cold, temperature, the coin, the autopsy, the continuous scale |
| 6 | rhythm, the swing, the kite, the wind, the tide, the arc, fit |
| 7 | the ledger, cause and effect, the free loaf, giving and extracting, the bay, the net |

Everything not in a principle's own row is borrowed.

---

## The rubric, 100 points

### Principle fidelity: 35

Is each law being used for what it actually governs, in its own terms?

| Band | What it looks like |
|---|---|
| 32-35 | The laws generated the findings. At most one section is thin enough that it would be true of any company in that industry, and the rest name something only this company does. No borrowed imagery anywhere. Where two laws touch, the domain owner argues it and the other references it in a clause. |
| 26-31 | Mostly right. Two sections state the law rather than using it, or one finding sits in the wrong domain. |
| 18-25 | Two or more sections are framework applied from outside: a generic business observation with a law's name attached. |
| 8-17 | The laws are headings over consulting boilerplate. Imagery mixed. |
| 0-7 | Wrong law, wrong domain, or the framework is decorative. |

**Imagery is not required in every section.** The benchmark uses one image in seven
sections and it is right to. What is scored is whether the imagery present is the law's
own, and whether the law's logic drove the finding. A section can carry no metaphor at all
and still be a 35, if the finding could only have come from that law. Deduct for a
borrowed image, never for an absent one.

The surest sign a law was not applied: a section that would be true of any company in that
industry. Read each one and ask whether it names something only this company does.

### Evidence grounding: 20

Does every claim trace to something real, and are the holes shown?

| Band | What it looks like |
|---|---|
| 18-20 | Every claim traces to the intake record. Observations attributed where they came from. Hedges present where the author heard something once. At least one gap written into the document as a gap, with the questions handed back. |
| 14-17 | Grounded, but one or two claims are stated flatter than the evidence supports. |
| 9-13 | Several unsupported claims, or a gap papered over with a plausible guess. |
| 4-8 | Largely inference dressed as observation. |
| 0-3 | Fabrication, anywhere. Also hard fail 2. |

Any invented fact puts this dimension at 0-3 regardless of how well-sourced the rest is.
One fabrication contaminates a document, because the reader who finds it stops trusting
the parts that were true.

The move that earns the top band: crediting what was learned before naming what was not.

### Actionability: 15

Can the owner start something this month, and do they know which one first?

| Band | What it looks like |
|---|---|
| 14-15 | Every section names at least one move that is specific, sized to this company, and startable now. Principle 7 walks them in an order the owner can follow. |
| 11-13 | Actionable, but one or two recommendations are a direction rather than a move, or nothing tells the owner where to begin. |
| 6-10 | Advice at the level of "improve your marketing" or "be more consistent". |
| 0-5 | Observation with no opening named. |

"Build a body of useful work" is not a move. "Six assets, these six, starting with the case
study from the customer who looked like them" is a move.

The full assessment does not carry a ranked list. Ordering lives in the Quick Read and in
Principle 7's walk. Do not deduct for the absence of a numbered ranking in the long
document.

**Deduct two, separately from the band**, when a recommendation carries a real cost, a
legal exposure, a regulatory question, or something the owner would have to stop doing, and
the document does not say so. Recommendations that are all upside read as a pitch. This is
the most common substantive omission in an otherwise strong draft: putting customer records
through new tooling at a company that handles regulated data, telling a nine-person firm to
build six assets in its busy season, recruiting operators under someone's brand. Name the
cost or name nothing.

### Voice: 20

Does it sound like one person talking to another?

**Register sets the band. Word-level tells are deductions inside it.** Score the band on
how the document reads as a whole, then subtract for individual tells down to the band's
lower bound and no further. A document whose register is right does not fall to 13 because
it contains seven cuttable words; it falls to 18. Structural tells are different: those
change the band.

| Band | What it looks like |
|---|---|
| 18-20 | First and second person throughout. Short paragraphs, sentence length varies. Confidence lives in the specifics. Client vocabulary used verbatim. No structural tells. |
| 14-17 | Register right, with one structural tell: a stack of staccato lines, a run of manufactured rhythm, a paragraph built out of balanced pairs. |
| 9-13 | Reads like a consulting report rather than a letter. |
| 4-8 | Corporate register throughout, or tells in every paragraph. |
| 0-3 | Unreadable as Mo. |

Deduct one point each, to the band floor, for: an em dash, or a spaced hyphen doing an em dash's work ("your messaging - both internally and externally"), a corrective negation, a
rule-of-three used for rhythm, a throat-clearing opener, a corporate verb (including
*leverage* as a verb, *foster*, *streamline*, *utilize*, *robust*, *seamless*), a filler
intensifier, a banned word (compounds, the gap between, most people, business-sense
friction or noise, "land" as a verb, figurative quietly, "exactly" as an intensifier), a
third-person reference to the reader ("the client", "the organization", "stakeholders").
Using the company's actual name is not a third-person reference and never deducts; the
reference assessment names the company throughout.

### Structure and completeness: 10

| Band | What it looks like |
|---|---|
| 9-10 | All seven sections, correct headings, correct order. Framing paragraph takes a position in its first two sentences. Seven-principles diagram directly under the framing paragraph, differentiator paragraph after the diagram. Section lengths vary with what was learned. Principle 7 is the synthesis. Closing sentence uses the owner's own words for their goal. |
| 7-8 | Complete, one structural element off. |
| 4-6 | Sections padded to uniform length, or the framing paragraph summarizes instead of taking a position. |
| 0-3 | Missing sections or wrong shape. |

The headings, exactly: `PRINCIPLE 1: Intent & Action`, `PRINCIPLE 2: Big & Small`,
`PRINCIPLE 3: Be Consistent`, `PRINCIPLE 4: Active & Passive`,
`PRINCIPLE 5: Winning & Losing`, `PRINCIPLE 6: Rhythm & Fit`,
`PRINCIPLE 7: Karma & Value`.

Padding is the most common failure here. A document where all seven sections run three
paragraphs was written to a template rather than from an interview. The benchmark's
unevenness is honest.

A full assessment under 900 words of prose has not been written from an hour of interview.
Say so, and deduct two from structure. Between 900 and 1,200 is thin but can be honest when
the interview was short; note it without deducting. The benchmark runs about 1,150.

---

## Six checks the bands do not cover

Run these separately and report anything they catch under FLAGGED. Each is worth a
deduction in the dimension it touches, and each is something a paying owner notices before
they notice an em dash.

1. **Contradiction.** Does any section contradict another? A document that says leadership
   lacks clarity in Principle 1 and that everything is working in Principle 5 destroys its
   own credibility faster than any other failure. Deduct from principle fidelity.
2. **The question they asked.** Did the document address the problem the owner brought,
   in the terms they brought it? Deduct from actionability.
3. **The citation.** If there is an outside source, is it named specifically enough that
   the reader could find it, and does the link look real? Flag anything you cannot check.
4. **The diagram against the prose.** If a marketing garden figure is present, does it list the
   assets the prose names? An empty slot is fine when the prose says the slot is empty. Mismatches are common and they read as carelessness.
5. **Named staff.** Every observation attached to a person's name should be one the owner
   could show that person. This document gets forwarded. "Rafa knows every parcel in the county by feel" is fine. A judgment about someone's competence is not.
6. **What it costs.** Where a recommendation has a real cost, a legal exposure, or requires
   the owner to stop doing something, does the document say so? Recommendations that are
   all upside read as a pitch.

---

## Thresholds

| Score | Verdict |
|---|---|
| 95-100 | Ship it. |
| 90-94 | Ship it. Note the flagged passages so the author sees them. |
| 80-89 | Close. Fix the flagged passages and score again. Does not ship. |
| 65-79 | Real problems. Usually a thin intake showing through. Rewrite the weak sections from evidence. |
| Below 65 | Start over from the intake record. |
| Any hard fail | Does not ship at any score. |

---

## Output format

```
7EIU PRINCIPLE FIDELITY, <document name>

INTAKE RECORD: <supplied | not supplied, evidence grounding unscored>

HARD FAILS: <none | numbered, each with the quoted line>

TOTAL: <n>/100   <verdict>

  Principle fidelity      <n>/35
  Evidence grounding      <n>/20
  Actionability           <n>/15
  Voice                   <n>/20
  Structure               <n>/10

FLAGGED
  <Principle N>, "<quoted passage>"
      <what is wrong, in one sentence, and what would fix it>
  ...

NOTE
  <Three or four sentences. What the draft does well, the one change that would move it
  most, and whether the underlying problem is the writing or the interview.>
```

Quote the actual text when you flag something. A flag without a quote is not useful to the
person fixing it.

Under 90, say plainly which sections to rewrite and whether the fix is in the prose or back
in the intake. Those are different problems and they need different work.
