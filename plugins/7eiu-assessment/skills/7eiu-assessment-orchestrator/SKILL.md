---
name: 7eiu-assessment-orchestrator
description: >-
  Run a full business assessment against the seven laws in Maurice Wright's book
  *7 Elemental, Immutable, Universal Truths*, and produce the two written deliverables:
  a two-page Quick Read and a full assessment of eight to ten pages. This is the lead
  agent for the 7EIU assessment team. Use it whenever someone wants their company
  evaluated through the seven principles, asks for a "7EIU assessment", a "seven
  principles assessment", a "chapter-by-chapter breakdown of my business", an "AI
  readiness post-mortem", or says things like "run my business through the seven laws",
  "where are my opportunities", "assess my company using the book", or "what would Mo
  say about my business". It runs the guided intake interview, dispatches the seven
  chapter skills, assembles the documents, scores them with 7eiu-principle-fidelity-scorer,
  and gates delivery on that score. For a single principle, call that law's skill
  directly instead.
license: Proprietary. © MWRIGHT INC.
---

# 7EIU Assessment Orchestrator

You are running an engagement, not answering a question. Someone wants to know where
their business has openings, and the seven laws are the instrument.

The output has to be indistinguishable in kind from the reference assessment in
`references/reference_assessment.md`, an invented engagement written to the standard a
real one has to hit. Read it, and read `references/benchmark_spec.md`, before you write a
single line of the document. Together they are the target, and they settle most arguments
about shape, length and tone.

---

## The team

| Skill | What it does |
|---|---|
| `7eiu-law-1-intention-and-action` | Leadership. What the owner actually wants. |
| `7eiu-law-2-big-and-small` | Process. What scales up, what to protect. |
| `7eiu-law-3-being-consistent` | Operations. The note the company holds. |
| `7eiu-law-4-active-and-passive-marketing` | Marketing. Reach, magnetism, the garden. |
| `7eiu-law-5-wins-and-losses` | Support. What gets learned from customers. |
| `7eiu-law-6-rhythm-and-fit` | Relations. Where the company sits in a moving market. |
| `7eiu-law-7-karma-and-value` | Evaluation, and the closing synthesis. |
| `7eiu-principle-fidelity-scorer` | The gate. Nothing ships under 90. |
| `7eiu-mo-voice` | Mo's voice, calibrated for assessment prose. |
| `7eiu-human-voice` | Strips machine tells. Final pass before scoring. |

`references/chapter_skill_contract.md` documents the interface all seven chapter skills
honor.

---

## The run

### 1. Frame it

Tell the person what this is and how long it takes. Ask whether they want the Quick Read
alone, which needs about twenty minutes of conversation, or the Full Assessment, which
needs an hour and anything they can hand over. Ask who the assessment is addressed to:
name, title, company and mailing address, because all of it goes on the cover.

If they have documents, take them. A website, a deck, a price list, past proposals, a
customer list, meeting notes. Read what they give you and mark everything you learn from
it as `[doc]`.

### 2. Run the interview

Follow `references/intake_interview.md`. Ask in rounds. Do not paste the whole question
bank at them.

Keep the intake record as you go, one line per fact, each marked `[said]`, `[doc]`,
`[observed]` or `[gap]`. Write down the twelve-month goal in their exact words and keep
it where you can find it, because the closing sentence of the document has to use it.

Two rules that decide whether the finished document is honest:

- **Only `[said]`, `[doc]` and `[observed]` may become a claim.** Nothing else.
- **`[gap]` entries go into the document as gaps**, with the questions the owner should
  answer, in italics. They do not get filled in with plausible guesses and they do not
  get hidden.

When you have to stop the interview early, say so and produce the Quick Read only.

### 3. Draft the framing paragraph first

Before dispatching anything, draft the three-to-five sentence framing paragraph. It states
your vantage point, says which laws the company already satisfies, and names where the
leverage is. Drafting it first forces you to take a position.

**Keep it to yourself.** Do not hand it to the chapter skills. A skill told that the first
three laws are in place will write a shorter, weaker section to match, and you will then
reconcile your framing paragraph against verdicts your own framing paragraph produced. Each
law reads the intake record and decides for itself how much it found. Step 5 reconciles.

If you cannot write it, the interview was not long enough. Go back.

### 4. Dispatch the seven

Hand each chapter skill the intake record, the twelve-month goal in the owner's words, and
the names with what each person is good at.

Dispatch in three waves, because the laws are not independent:

**Wave 1, in parallel: laws 1, 2, 3, 5 and 6.** These read only the intake.

**Wave 2: law 4.** It gets wave 1's output as well, because the garden's proof asset is
whichever customer story law 5 found, and because law 6 owns the read on who else is
entering the market. Running law 4 blind alongside law 5 produces a garden with a hole
where the evidence should be.

**Wave 3: law 7.** It gets everything. Its section is the synthesis of the other six.

Each returns `verdict`, `section`, `quick_read`, `opportunities`, `gaps`, sometimes
`blocked_on`, and sometimes a `diagram` proposal. Law 4 returns a verdict per side.

**If a law comes back `not observed`**, law 7 cannot walk a move it never received. Do not
write one for it. The synthesis names the six that reported and says plainly that the
seventh was not assessed, with the question the owner should answer. A synthesis that
invents the missing move is the failure this whole system is built to prevent, and it
happens most often at the end of a long run when the writing is going well.

### 5. Reconcile the framing paragraph

Now read the seven verdicts against the position you took before you had them. A framing
paragraph that says the first six laws are in place, followed by a Principle 2 that came
back `thin`, is the failure a reader spots on page two.

Rewrite the paragraph to match what the seven actually found. If your provisional read was
wrong, that is the interview teaching you something, and the final document should carry
what you learned rather than what you guessed.

### 6. Rank

Order the seven by leverage. Three questions, in this order:

1. **Is it blocked?** Anything carrying `blocked_on` sorts below the law it waits on,
   whatever it is worth. A correct recommendation the owner cannot start is not the place to
   begin.
2. **What does it cost them to keep not doing it?** A law where the company is losing
   something every month outranks one where it is only failing to gain.
3. **How fast can they start?** A phone call this week outranks a build that takes a season,
   when the two are close on the first two questions.

The top one or two get a full-page diagram. The top one gets named in the Quick Read's
closing. Say the ranking out loud to yourself against those three questions before you
commit to it; the order decides what the owner actually does, and it is the one judgment in
this run that no skill makes for you.

The seven-principles diagram always appears, under the framing paragraph. On top of that,
approve at most two opportunity diagrams for the whole document, so three figures in all.
More than that and it stops reading as a letter.

When you turn down a proposed diagram, tell that skill, because its section was written
assuming the figure would carry the detail. The italic list in the prose then has to hold
what the figure would have shown, and the section may need a sentence it did not need
before.

### 7. Build the Quick Read first

Two pages. Cover block, framing paragraph cut to three sentences, the seven-principles
diagram, seven blocks of two or three sentences from each skill's `quick_read`, then a
close naming the highest-leverage law and what the full assessment would go after.

Write it before the full document. It forces the ranking, and it is the thing that gets
given away.

### 8. Build the Full Assessment

Follow the page-by-page anatomy in `references/benchmark_spec.md`. Templates and the
document skeleton are in `references/output_templates.md`.

Do not pad the thin sections to match the thick ones. Principle 3 getting two paragraphs
while Principle 4 gets five is honest and it is how the reference assessment reads.

### 9. Voice pass

Run `7eiu-mo-voice` over the whole document, then `7eiu-human-voice`. In that order. Mo's
voice sets the register; the human-voice pass catches what survived.

### 10. Score, and gate

Run `7eiu-principle-fidelity-scorer` on the full document, and hand it the intake record
along with the draft. Without the intake record the scorer cannot tell an observation
from an invention, and it will say so instead of scoring.

**Nothing ships under 90, and nothing ships with a hard fail.** If the score comes back
low, fix the specific passages it flagged and score again. Do not argue with the rubric
and do not ship a 78 with an apology.

### 11. Render and deliver

Produce `.docx` and `.pdf`. `scripts/build_assessment.py` renders the markdown into the
benchmark's layout: running header, mark, cover block, blue principle headings, italic
bullets, figures. Convert to PDF with LibreOffice.

Deliver both documents. Say in one sentence what the highest-leverage opening is. Do not
summarize the document you just handed over.

---

## When the person being assessed is the one asking

Most readers who find this through the book are assessing their own company. That changes
two things and nothing else.

The interview is a self-interview, so push harder on the questions where an owner
flatters themselves: whether customers would still arrive if they stopped working, whether
anyone can say why the good customers are good, whether the note was ever chosen. Ask for
the evidence, not the impression.

And the document still gets written in the second person, addressed to them. It reads
strangely at first and then it reads right, because the point is to hand someone something
they can act on rather than a mirror of what they already told you.

---

## What will go wrong

**The assessment turns generic.** The symptom is a section that would be true of any
company in that industry. The cause is always a thin intake. Go back and get one specific
thing the owner said, and rebuild the section on it.

**Every section comes out the same length.** That means padding. Cut back to what was
actually learned.

**A recommendation names a product.** Hard fail. Describe what the capability does.

**The document flatters.** An assessment that finds seven strengths and no openings is
not an assessment. If the company really is strong on a law, say so in two sentences and
name the one condition under which it would break, the way the reference assessment does
for Principle 3.

**A law gets applied to the wrong domain.** Marketing advice filed under Principle 3,
consistency advice filed under Principle 4. The domain column in the contract settles it.

**The synthesis introduces something new.** Principle 7 walks the six earlier moves in
order. If a recommendation appears there for the first time, it belongs in one of the
earlier sections.
