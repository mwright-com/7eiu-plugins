# Output templates

Two documents come out of one intake. Both are written as markdown with the front-matter
block below, then rendered by `scripts/build_assessment.py`.

---

## Front matter (both documents)

```yaml
---
doc_type: full            # full | quick
client: Clear RCM
engagement: AI Readiness Training
kicker: POST MORTEM       # or DIAGNOSTIC, or ASSESSMENT
subtitle: An evaluation using the 7 EIU principles
prepared_for:
  name: Brian Shields
  title: Chief Executive Officer, Clear RCM
  address:
    - 4500 Eldorado Pkwy, Ste 2100
    - McKinney, TX 75070
prepared_by:
  name: Maurice Wright
  company: MWRIGHT INC
  city: Berkeley, CA
  email: mo@mwright.com
  phone: 510-453-2289
focus_law: 7              # the law highlighted in the diagram
goal_verbatim: "growth thesis"
---
```

`goal_verbatim` is the owner's own phrase for what they are trying to do. The closing
sentence of the full document has to contain it.

---

## The Quick Read

Two pages. Given away. It has to be good enough that someone would pay for the long one.

```markdown
## <one-line read on where this company stands>

<Framing paragraph, three sentences. Vantage point, which laws are already in place,
where the leverage is.>

![7 Principles Diagram](figures/seven_principles.png)

**PRINCIPLE 1: Intent & Action**
<Two or three sentences. One observation, one opening.>

**PRINCIPLE 2: Big & Small**
<Two or three sentences.>

**PRINCIPLE 3: Be Consistent**
<Two or three sentences.>

**PRINCIPLE 4: Active & Passive**
<Two or three sentences.>

**PRINCIPLE 5: Winning & Losing**
<Two or three sentences.>

**PRINCIPLE 6: Rhythm & Fit**
<Two or three sentences.>

**PRINCIPLE 7: Karma & Value**
<Two or three sentences.>

### Where I would start

<Name the single highest-leverage law and the first move under it. Then one sentence on
what a full assessment would go after that this could not. End forward-looking. No
sales pitch and no manufactured closing line.>
```

Rules for the Quick Read:

- Each block is written fresh from the chapter skill's `quick_read`, not trimmed from the
  long section.
- Every block names something the owner actually said. If a block cannot, that law is
  `not observed` and the block says so in one sentence and asks the question.
- No diagram other than the seven principles.
- No page of methodology. Nobody reads it.

---

## The Full Assessment

Eight to twelve pages. The benchmark.

```markdown
<Framing paragraph. Three to five sentences. Vantage point, which laws are already in
place, where the leverage is.>

![7 Principles Diagram](figures/seven_principles.png)

<Differentiator paragraph. One paragraph on what this company has that is not the
product. Comes from the "what do you have that is not the product" question.>

<One-line hand-off. Something like: Assuming that you already know this, the next step
is to run the growth phase through the seven principles.>

**PRINCIPLE 1: Intent & Action**

<One to three short paragraphs.>

**PRINCIPLE 2: Big & Small**

<One to four short paragraphs. Names people by first name where the intake supports it.>

**PRINCIPLE 3: Be Consistent**

<One to three short paragraphs.>

**PRINCIPLE 4: Active & Passive**

<Two to five short paragraphs. Italic bullets for the asset menu.>

![The Marketing Garden](figures/marketing_garden.png)

**PRINCIPLE 5: Winning & Losing**

<Two to four short paragraphs. Italic bullets for the questions handed back.>

**PRINCIPLE 6: Rhythm & Fit**

<Two to four short paragraphs. Real, linkable outside reference if there is one.>

**PRINCIPLE 7: Karma & Value**

The previous 6 principles suggest the following:

<One paragraph walking the six earlier recommendations in law order, in the owner's own
terms. Closing sentence states what you believe about them reaching the goal they named,
using `goal_verbatim`.>
```

---

## Figures

Two are built in. Others are made only when a chapter skill proposes one and the
orchestrator approves it, at most two per document.

**`seven_principles.png`** is always present, directly under the framing paragraph.
Source: `diagram_seven_principles.html`. Three groups across the page. MANIFESTING
THOUGHT holds laws 1 to 3 with the domain labels LEADERSHIP, PROCESS, OPERATIONS.
BUILDING RELATIONSHIPS holds laws 4 to 6 with MARKETING, SUPPORT, RELATIONS. REFLECTION
holds law 7 with EVALUATION, in its own tall panel on the right. The focus law's card is
tinted. Each card carries the domain word small and grey above the law name in bold, with
a large ghosted numeral in the corner. Caption: `7 Principles Diagram`.

**`marketing_garden.png`** appears when Principle 4 carries the leverage, which is often.
Source: `diagram_marketing_garden.html`. A header card naming the asset that already
exists, with the law stated in the client's terms beside it. Then six cards on a spine:
PROOF, CAPTURE, DIAGNOSTIC, AUTHORITY, CADENCE, ACCESS. Each has the category word in
blue, the asset name in bold, and one line of what it is for. Footer line ties it back to
what the tools make possible. The slot names are fixed. The assets are chosen from what
this company actually knows.

Other diagrams follow the same visual grammar: a title in wide-tracked caps on the left,
the principle number on the right, a rule under both, then cards. Nothing decorative.

---

## Layout constants

Held in `scripts/build_assessment.py`.

- US Letter, 1 inch margins.
- Running header: author name and city left, email and phone right, 9 pt grey.
- Mark centered under the header on every page.
- Body: 11 pt Arial, 1.5 line spacing. This is a business document, not the book, so it
  does not use the book's Garamond.
- Principle headings: 10 pt bold, brand blue, small caps feel from the wording itself.
- Title: 28 pt bold brand blue, centered. Kicker above it in wide-tracked grey caps.
  Subtitle below in grey.
- Bulleted lists: italic, one line each.
- Page numbers: centered at the foot.
- Brand blue: `#1F5FBF` for headings and rules, `#0B3D91` for the title.
