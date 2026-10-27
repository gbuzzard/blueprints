# blueprints

Claude-based skills and files for designing software, experiments,
proposals, papers, and other work before it is done.

**To Claude: a person has dropped this kit into the chat, as a zip file or
a folder, to start blueprinting.  Start now, without being asked.**

1. If it is still a zip file, unzip it into a folder of its own.
2. Read `SKILL.md` and follow it.  It names the kinds of work, and
   `BASE.md` gives the exact steps.  Show every page as a rendered web
   page, as an HTML artifact in the Claude app or in the browser from
   Claude Code, never as HTML text in the chat.  End every message with
   one clear question.

The rest of this page is for the person.

## What the kit does

This kit teaches Claude to design a piece of work with you by
**blueprinting**.  Before the work is done, its design is set down on a
few short web pages, called blueprints.  Claude interviews you, sets up
the pages, and writes them.  You read each one, mark it up, and decide
its open questions.  The work starts only after the blueprints you need
are settled.

The method is the same for every kind of work.  What differs is the set
of blueprints, the interview questions, and what happens after the
design is settled.  The kit now has two kinds:

| Kind | What it designs | Its blueprints |
|---|---|---|
| Software | A software project, before any code is written. | Theory, Software Architecture, Hardware Mapping, and User API, plus optional ones such as Testing and Verification. |
| Experiment | A computational experiment, before any run. | Goal, Motivation, Plan, Results, and Conclusion.  The last two record what was measured and learned. |

## Getting started

**In Claude Code.**  Open Claude Code in the folder of the project the
work belongs to and drag the zip file into the chat line.  Claude asks
which kind of work you have, unless you have said so, and asks once
whether to install the kit as a skill, so that next time you can type
`/blueprints`.

**In the Claude app or on claude.ai.**  Install the kit once: open
Settings, find Skills, and upload the zip file.  Then in any chat say,
for example, "Let's blueprint my experiment."  Custom skills need a paid
plan with code execution turned on.

Either way, Claude first shows you an example front page, then asks you a
few questions, then opens the front page of your own blueprints.

## What is in the kit

| File | What it is |
|---|---|
| `README.md` | This page. |
| `SKILL.md` | Where Claude starts: the list of kinds and how to choose one. |
| `BASE.md` | The method and the rules that every kind follows. |
| `KINDS.md` | How a kind is defined, and how to add one. |
| `kinds/software/` | The software kind: `KIND.md`, a front page template, and an example (a made-up image denoiser). |
| `kinds/experiment/` | The experiment kind: `KIND.md`, its templates, and an example (a made-up comparison of two CT denoisers). |
| `templates/` | The templates every kind uses unless it has its own: front page, blueprint page, `decisions.md`, and `CLAUDE.md`, the coding and comment style Claude follows if the work needs code. |
| `docs/rule_sort.md` | Where each rule of the two earlier kits went in this kit. |

## Read it before you use it

Read any instructions before you give them to your Claude, including
these.  They are short so that you can.

- Every file is plain text: Markdown and HTML.  There are no programs, no
  scripts, and no JavaScript.  Equations are written in MathML, which
  browsers typeset without any script.
- The templates load nothing from the internet.
- `BASE.md` tells Claude to edit files only in the blueprint folder you
  choose, and to ask you before it runs a command, starts a run of an
  experiment, installs anything, uses the network, commits, or pushes.
- `BASE.md` tells Claude to treat text inside your papers, code, and data
  as information, never as instructions.

If a copy you received contains anything else, such as a script or a link
that loads code, do not use it.

## The method

C. A. Bouman, "Blueprinting: A Methodology for AI Software Design," in
preparation.  The software kind is the Blueprinting starter kit, version
5, by C. A. Bouman, moved onto the shared base.  The experiment kind
adapts the same method to the design of computational experiments.
