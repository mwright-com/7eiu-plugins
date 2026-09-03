# 7EIU Plugins

Tools that come with *7 Elemental, Immutable, Universal Truths: for Building What People
Want with AI*, by Maurice Wright.

[book.mwright.com](https://book.mwright.com)

---

## New here? → **[START-HERE.md](plugins/7eiu-assessment/START-HERE.md)**

Plain language, no jargon, five minutes. That is the right first stop whether or not you
write code.

---

## The 7EIU Assessment Team

A team of AI helpers that reads a business and writes an assessment of it, organized by the
seven laws.

Think of a home inspection. A lead inspector walks around with the owner asking questions.
Specialists each check one thing. The lead turns all of it into one report. This does that
for a business, and the seven things it checks are the seven laws.

You get two documents: a two-page read you can hand to anyone, and a full assessment of
eight to ten pages.

Twenty minutes of conversation gets the short one. About an hour gets the long one.

### Install

**In the Claude app or on claude.ai** (most people, no terminal):

1. **Customize** in the left sidebar.
2. Click the **Plugins** icon in the panel's left icon strip. It is the plug, fourth
   one down, and it is easy to miss: Skills and Plugins are separate panels, and the
   Skills one has no repository option at all.
3. **Add** → **Add marketplace** → **Add from a repository**.
4. Type `mwright-com/7eiu-plugins`, click the **Use "mwright-com/7eiu-plugins"** suggestion,
   then **Sync**.
5. Click **Add** beside **7eiu assessment**.

In Cowork, open the Cowork tab first.

**In Claude Code**, the terminal tool:

```
/plugin marketplace add mwright-com/7eiu-plugins
/plugin install 7eiu-assessment
```

Those two lines are Claude Code only. They do nothing typed into a chat window.

### Use

```
Run my business through the seven principles.
```

Answer the questions like you would answer a person. That is the whole interface.

---

## What's inside

Eleven skills. A lead that runs the interview and assembles the document, one specialist per
law, a scoring rubric that gates the output, and two skills that handle voice.

Every skill is a single Markdown file of instructions. There is no service, no account, and
nothing running in the background. Your business information goes wherever your AI
conversation already goes, and nowhere else.

| | |
|---|---|
| **[START-HERE.md](plugins/7eiu-assessment/START-HERE.md)** | Plain language. Start here. |
| **[USAGE.md](plugins/7eiu-assessment/USAGE.md)** | Operator's manual. How it fits together and how to change it. |
| **[LICENSE.md](plugins/7eiu-assessment/LICENSE.md)** | What you may and may not do with it. |

---

## How it stays honest

Three rules, and the scoring skill enforces all three.

**Nothing gets claimed that you did not say.** Every fact traces back to the interview or a
file you supplied. Where the conversation did not reach, the document says so and hands the
questions back to you rather than filling the hole with a guess.

**No AI product names, ever.** The document says what a capability does, never what it is
called. Products change every few months. The seven laws do not.

**Nothing ships under 90 out of 100.** Five dimensions, eight automatic failures, and six
checks for what a business owner notices before they notice a typo: contradictions between
sections, whether the document answered the question you actually asked, whether any
recommendation with a real cost says so.

---

## Contributing

This repository does not take outside changes. Issues and pull requests are closed, and the
license does not permit modified copies.

If you have found a problem, or you want to adapt this for your own practice, write to
**mo@mwright.com**. That is a conversation worth having and the door is open.

---

© MWRIGHT INC. All rights reserved. See [LICENSE.md](plugins/7eiu-assessment/LICENSE.md).
