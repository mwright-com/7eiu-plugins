# Start here

This is a team of AI helpers that reads a business and writes an assessment of it, using
the seven laws from *7 Elemental, Immutable, Universal Truths*.

**You do not need to be technical to use it.** If you can have a conversation, you can run
it. The technical parts are for people who want to change how it works.

---

## What it actually does

Think of a home inspection.

Someone wants to know what's wrong with their house. A lead inspector walks around with the
owner, asking questions. Then specialists each check one thing: roof, wiring, plumbing.
Each writes down what they found. The lead turns all of it into one report.

This does that for a business. The seven things it checks are the seven laws from the book.

You end up with two documents:

- **A two-page read.** Short. Good for handing to someone who has not hired you yet.
- **A full assessment, eight to ten pages.** The real deliverable.

---

## Running it

Install it (see below), then just ask:

```
Run my business through the seven principles.
```

It will start asking you questions. Answer them like you would answer a person. Twenty
minutes gets the short document. About an hour gets the long one.

Bring anything you have. A website, a price list, old proposals, notes from a meeting. It
reads what you give it.

Other ways to ask:

```
Assess my company using the 7EIU framework and give me the full write-up.

Just the quick read, I have twenty minutes.
```

Or ask about one law on its own, when you have one symptom rather than a whole question:

```
Principle 4 only. Where is my marketing one-sided?

Run principle 6 on us. Why is this so much work for so little return?
```

---

## Installing it

### In the Claude app or on claude.ai

This is the path for most people. No terminal.

1. Click **Customize** in the left sidebar.
2. In the narrow icon strip on the left of the panel, click the **Plugins** icon (the plug,
   fourth one down). This is easy to miss: Skills and Plugins are separate panels, and the
   Skills panel has no repository option at all.
3. Top right, click **Add**, then **Add marketplace**.
4. Choose **Add from a repository**.
5. Type `mwright-com/7eiu-plugins` in the box, then click the **Use "mwright-com/7eiu-plugins"**
   line that appears below it.
6. Click **Sync**.
7. **7eiu assessment** now appears in the list. Click **Add** beside it.

You should see "7eiu assessment is installed and ready to use."

In Cowork, open the Cowork tab first, then Customize.

### In Claude Code (the terminal tool)

```
/plugin marketplace add mwright-com/7eiu-plugins
/plugin install 7eiu-assessment
```

**These two lines only work in Claude Code.** Typing them into a normal chat window does
nothing. If you are not working in a terminal, use the app steps above.

### Either way

Nothing else to set up. The helpers load when they are needed and stay out of the way when
they are not.

---

## What you get, and what it costs you

**Time.** Twenty minutes to an hour of conversation, once.

**Honesty.** The assessment will tell you things you did not want to hear. That is the
point of it. An assessment that finds seven strengths and no openings is not an assessment.

**Nothing else.** There is no account to make, no data sent anywhere, no subscription.

---

## Three promises the tool keeps

**It will not make things up about your business.** Every claim in the finished document
traces back to something you said or a file you handed over. Where the conversation did not
go deep enough, the document says so and hands you the questions rather than guessing.

**It will not name AI products.** It says what a capability does, never what it is called.
Products change every few months. The seven laws do not, and a document full of this year's
product names is out of date before you have acted on it.

**It will not flatter you.** There is a scoring step that grades the finished document and
refuses to release it below 90 out of 100. Padding, vagueness, and made-up specifics all
lose points.

---

## For the technical reader

Everything above is the whole story for most people. If you want to look under the hood:

- **[`USAGE.md`](USAGE.md)** is the operator's manual. How the eleven skills fit together,
  how the document gets built into Word and PDF, how to change any of it.
- **`skills/`** holds the eleven skills. Each is a single Markdown file of instructions.
  There is no code to speak of, and nothing runs in the background.
- **`skills/7eiu-assessment-orchestrator/references/`** holds the shared library: the
  document target, the interview questions, the interface every chapter skill honors, and a
  complete worked example.
- **`skills/7eiu-assessment-orchestrator/scripts/build_assessment.py`** turns the finished
  assessment into a formatted Word file. Needs `python-docx`.

---

## Questions people ask

**Do I need to know anything about the book?**
No. The assessment explains itself as it goes. The book makes it land deeper, and the tool
works without it.

**Can I use this on a client's business, not my own?**
Yes. That is what it was built for. Drop a `mark.png` beside the assessment and it goes out
under your brand instead.

**Is my business information going anywhere?**
It goes wherever your AI conversation already goes and nowhere else. This adds no storage,
no server, and no account. It is a set of written instructions.

**What if the assessment is wrong about something?**
Tell it. It was built from one conversation, and a conversation can miss things. Correcting
it and asking for that section again is normal use, not a failure.

**Can I change how it works?**
Read the license first. Then see `USAGE.md`.

---

*7 Elemental, Immutable, Universal Truths: for Building What People Want with AI*
Maurice Wright · [book.mwright.com](https://book.mwright.com)
