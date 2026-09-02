# Running the 7EIU Assessment Team

Eleven skills that interview a business owner, work each chapter of *7 Elemental,
Immutable, Universal Truths* in turn, and write the assessment.

This file covers what shipped, how to install it, how to run an engagement, and what to
do when the output comes out wrong.

---

## 1. Which archive to use

Three archives went out. The same eleven skills are in all three. What differs is how they
get installed and who does the installing.

| Archive | For | What it is |
|---|---|---|
| `7eiu-assessment-plugin.zip` | Readers | The installable plugin: manifest, README, this file, and the eleven skills. This is the thing a reader installs. |
| `mwright-book-marketplace.zip` | book.mwright.com | A marketplace named `mwright-book` with the plugin inside it. Host this and readers install by name instead of by folder. |
| `7eiu-assessment-skills.zip` | You | The eleven skill folders alone, no plugin wrapper. Source of truth, and what to edit when you change something. |

**To try it yourself:** unzip `7eiu-assessment-skills.zip` and copy the eleven folders into
your skills directory. No plugin, no marketplace. Everything works, you just install it by
hand.

**To publish it:** host the marketplace. A reader then runs two lines and has the whole
team.

```
/plugin marketplace add mwright-book
/plugin install 7eiu-assessment
```

The plugin zip is what the marketplace serves. It is also the file to hand someone
directly when they cannot reach the marketplace.

---

## 2. Running an assessment

Ask for it in plain words. The orchestrator takes over.

```
Run my business through the seven principles.

Assess my company using the 7EIU framework and give me the full write-up.

Just the quick read, I have twenty minutes.
```

Twenty minutes of conversation gets the Quick Read. About an hour gets the full
assessment. Bring anything you have: a website, a deck, a price list, past proposals,
meeting notes.

### What happens, in order

1. **The interview.** Ten rounds. One on the company, one per law, one to close. Asked
   conversationally, not as a form. Every answer goes into an intake record.
2. **A position, taken early.** A three-sentence framing paragraph, drafted before
   anything is dispatched and kept private. Handing it to the chapter skills would bias
   them into writing short sections to match it.
3. **Three waves.** Laws 1, 2, 3, 5 and 6 in parallel. Then law 4, because the garden's
   proof asset is whichever customer story law 5 found. Then law 7, which synthesizes the
   other six.
4. **Reconcile, then rank.** The framing paragraph gets rewritten against what the seven
   actually found. Findings are then ordered: blocked ones sort below what they wait on,
   then by what it costs to keep not doing it, then by how fast you could start.
5. **Quick Read first, then the long one.** The short document gets written first, because
   writing it forces the ranking the long one needs.
6. **Voice, then the gate.** Mo's voice sets the register, the human-voice pass catches
   what survived, and the scorer decides whether it ships. Nothing goes out under 90.
7. **Render and send.** The build script produces the .docx. LibreOffice converts to PDF.

### One law on its own

Skip the orchestrator and call the chapter skill directly. Useful when someone has one
symptom rather than a whole question.

```
Principle 4 only. Where is my marketing one-sided?

Run principle 6 on us. Why is this so much work for so little return?
```

---

## 3. What comes out

**The Quick Read, two pages.** Cover block, a three-sentence framing paragraph, the
seven-principles diagram, and seven blocks of two or three sentences. Closes by naming the
one law with the most leverage. Free, ungated, built to be given away from the marketing
garden.

**The Full Assessment, eight to ten pages.** Cover, framing paragraph, diagram, the
differentiator paragraph, seven principle sections of uneven length, up to two opportunity
diagrams, and a closing synthesis that walks the six earlier moves in order and ends on
the owner's own words for their own goal.

> **The sections are meant to be uneven.** In the Clear RCM document, Principle 1 is one
> paragraph and Principle 4 is five plus a diagram. That is what was actually learned about
> each. Padding them to matching length is the most common way one of these documents goes
> wrong, and the scorer catches it.

---

## 4. Building the .docx and .pdf

```bash
# from the folder holding your assessment.md
python3 skills/7eiu-assessment-orchestrator/scripts/build_assessment.py \
        assessment.md --figures -o out

soffice --headless --convert-to pdf --outdir out out/Your_Client_Assessment.docx
```

The script needs `python-docx`. The `--figures` flag renders the two diagram templates to
PNG and needs a headless Chromium; it finds Playwright's bundled one if you have it.
Without a browser it skips the figures and still builds the document.

### Three files it looks for beside your markdown

| File | What it does | Required |
|---|---|---|
| `garden.json` | Fills the marketing garden figure: the anchor asset, the law in the client's terms, and the six slots. | Only when Principle 4 gets a diagram |
| `mark.png` | A brand mark, centered under the running header on every page. The MWRIGHT INC mark is packaged and used by default; a `mark.png` beside your assessment overrides it. | No |
| `figures/` | Where rendered diagrams land. Created for you. | Automatic |

**White-labelling the mark.** The packaged mark lives at
`skills/7eiu-assessment-orchestrator/assets/mark.png` and renders on every page without
any setup. To run an engagement under a client's brand, or someone else's, drop their
`mark.png` beside the assessment markdown; a mark found there wins over the packaged one.
Transparent PNG, trimmed to the glyph, and the layout scales it to 0.42 inches tall.

### garden.json

```json
{
  "anchor": "The Clear RCM website",
  "law": "Active marketing trades your team's time for a prospect's attention. A garden does not.",
  "foot": "Every asset above is buildable with AI tools, and costs no calendar time.",
  "slots": [
    {"asset": "Case studies",           "use": "Proof from a practice that looked like theirs."},
    {"asset": "Downloadable guides",    "use": "A guide they keep, with your name on it."},
    {"asset": "Self-assessment surveys","use": "A score on their own billing operation."},
    {"asset": "Local market reports",   "use": "Numbers for their market, not the nation's."},
    {"asset": "A newsletter",           "use": "A standing reason to be heard from."},
    {"asset": "Short explainer videos", "use": "One real question, answered fast."}
  ]
}
```

The six slot names are fixed: PROOF, CAPTURE, DIAGNOSTIC, AUTHORITY, CADENCE, ACCESS. The
assets are chosen from what the company actually knows.

### Front matter that drives the cover

```yaml
doc_type: full            # full | quick
client: Clear RCM
engagement: AI Readiness Training
kicker: POST MORTEM
subtitle: An evaluation using the 7 EIU principles
prepared_for:
  name: Brian Shields
  title: Chief Executive Officer, Clear RCM
prepared_by:
  name: Maurice Wright
  company: MWRIGHT INC
  city: Berkeley, CA
  email: mo@mwright.com
focus_law: 7              # the law tinted in the diagram
goal_verbatim: "growth thesis"
```

`goal_verbatim` is the owner's own phrase for what they are trying to do. The closing
sentence of the document has to contain it.

---

## 5. Three rules, enforced

### Nothing gets claimed that the owner did not say

Every fact in the intake record carries a source mark, and only three of the four may
become a claim in the document.

| Mark | Meaning |
|---|---|
| `[said]` | The owner or a team member said it in the interview. |
| `[doc]` | It came out of a file they supplied. The file gets named. |
| `[observed]` | You saw it yourself in something they showed you. |
| `[gap]` | You asked and did not get an answer, or did not ask. Never becomes a claim. |

Gaps do not get dropped and they do not get filled in with a plausible guess. They go into
the document as gaps, in italics, with the questions handed back to the owner. That move,
which the Clear RCM document makes under Principle 5, is what makes the rest of it
believable.

### No tool names, ever

The document says what a capability does, never what it is called. Same rule as the book,
and it is what stops the deliverable expiring. A draft naming a product does not ship,
whatever else it scores.

### The scorer decides, not the writer

Five dimensions to 100, eight hard fails, and six extra checks the bands do not cover:
contradiction between sections, whether the document answered the question the owner
actually brought, whether the one outside citation is real, whether the diagram matches
the prose, whether every named staff observation is one the owner could show that person,
and whether any recommendation carrying a real cost says so.

> **The Clear RCM document scores 92, and it ships.** It is not a 96, and the rubric says
> why rather than fudging it: Principle 1 is two sentences that would be true of any
> company, and no recommendation in it names a cost. 92 is what a very good assessment
> looks like. 90 is the gate. Nobody has hit 96 yet.

---

## 6. The eleven skills

| Skill | Domain | Job |
|---|---|---|
| `7eiu-assessment-orchestrator` | | Runs the engagement end to end. Holds the shared library. |
| `7eiu-law-1-intention-and-action` | Leadership | What the owner wants, and whether anyone downstream can tell. |
| `7eiu-law-2-big-and-small` | Process | Which large-company patterns to shrink, which instincts to protect. |
| `7eiu-law-3-being-consistent` | Operations | The note the company holds, and what breaks it. |
| `7eiu-law-4-active-and-passive-marketing` | Marketing | Reach, magnetism, and the marketing garden build-out. |
| `7eiu-law-5-wins-and-losses` | Support | Whether anything gets learned from how customers go. |
| `7eiu-law-6-rhythm-and-fit` | Relations | Where the company sits against a market that keeps moving. |
| `7eiu-law-7-karma-and-value` | Evaluation | Value created or extracted, and the closing synthesis. |
| `7eiu-principle-fidelity-scorer` | | The gate. Nothing ships under 90 or with a hard fail. |
| `7eiu-mo-voice` | | Mo's voice, calibrated for assessment prose rather than the book. |
| `7eiu-human-voice` | | Machine-tell pass, bundled so plugin users get it without account skills. |

### The shared library

Everything the seven chapter skills write against lives under the orchestrator, in
`references/`.

| File | What it settles |
|---|---|
| `benchmark_spec.md` | The document target. Shape, length, tone, hard fails. |
| `intake_interview.md` | The ten rounds, and how to record what you hear. |
| `chapter_skill_contract.md` | The interface, the imagery table, the contested findings. |
| `output_templates.md` | Both document skeletons and the layout constants. |
| `diagram_seven_principles.html` | The figure that sits under the framing paragraph. |
| `diagram_marketing_garden.html` | The Principle 4 opportunity figure. |
| `scripts/build_assessment.py` | Renders the markdown into the benchmark's layout. |

---

## 7. Editing and extending

Edit the folders in `7eiu-assessment-skills.zip`, then copy them back over
`7eiu-assessment/skills/` and re-zip. The plugin manifest and the marketplace entry do not
need touching unless you are bumping the version.

**Two things to know before editing a chapter skill.**

Each law owns a set of images and may not borrow another law's. That table lives in
`chapter_skill_contract.md`, and every chapter skill carries the whole thing rather than a
summary of it. A shortened copy is how an image goes missing from a forbidden list and
then turns up in a section, which is what happened during testing.

Four findings get claimed by two laws each, and the contract fixes an owner for every one,
so the same recommendation does not reach the client twice under two names: writing
something down, individual operators entering a market, customer stories, and what a
market pays a person for.

**Adding an eighth law.** Build it to the contract and the orchestrator picks it up
without changes. The hand-back block is `verdict`, `section`, `quick_read`,
`opportunities`, `gaps`, optionally `blocked_on` and a `diagram` proposal.

---

## 8. Troubleshooting

**The assessment reads generic.** A section that would be true of any company in that
industry means the intake was thin. Go back and get one specific thing the owner said,
then rebuild the section on it. This is an interview problem, not a writing problem, and
rewriting the prose will not fix it.

**Every section came out the same length.** Padding. Cut back to what was actually
learned. A document where all seven sections run three paragraphs was written to a
template.

**The document flatters.** An assessment that finds seven strengths and no openings is not
an assessment. When a law really is being obeyed, say so in two sentences and name the one
condition under which it would break.

**The garden gets recommended to someone with no time.** Working as intended if the section
also says so. A law that is right but blocked returns `blocked_on` naming the law that has
to move first, and the ranking sorts it below that one. If it did not, the chapter skill
skipped a step.

**The score comes back low.** The scorer says whether the fix is in the prose or back in
the intake. Those are different problems. Fix the flagged passages and score again rather
than shipping with an apology.

**Figures do not render.** No headless browser on the path. The document still builds, the
figure lines are skipped, and the script says so. Install Chromium or run the build
somewhere that has one.

---

*7 Elemental, Immutable, Universal Truths: for Building What People Want with AI*
Maurice Wright · [book.mwright.com](https://book.mwright.com)
