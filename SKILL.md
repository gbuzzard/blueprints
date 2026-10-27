---
name: blueprints
description: Design a piece of work with the user by blueprinting, before the work is done. The kinds are software (a project's theory, architecture, hardware mapping, and user API, before any code) and computational experiments (goal, motivation, plan, results, and conclusion, before any run). Use when the user asks to blueprint a project or an experiment, or to design software or an experiment before doing it.
---

# Blueprints

This kit holds one method, blueprinting, and several kinds of work it
applies to.  The method is in `BASE.md`.  Each kind has a kind file,
`kinds/<kind>/KIND.md`, that supplies what the method leaves open.

The kinds:

| Kind | Folder | What it designs |
|---|---|---|
| Software | `kinds/software/` | A software project, before any code is written. |
| Experiment | `kinds/experiment/` | A computational experiment, before any run, and afterward its results and conclusion. |

Start this way:

1. Read `BASE.md`.  Its safety rules come before anything else.
2. Choose the kind.  If the person's request names it, such as "blueprint
   my experiment," use that kind.  Otherwise ask:

   > Which kind of work do you want to blueprint: software or a
   > computational experiment?

3. Read the kind's `KIND.md`.  Where it states a rule that differs from
   a rule in `BASE.md`, the kind file's rule applies.
4. Read the templates and the kind's example.  For each template, use
   `kinds/<kind>/templates/<file>` when that file exists, and
   `templates/<file>` otherwise.
5. Follow `BASE.md` from Step 1.

Use one kind for one set of blueprints.  When a piece of work needs
another kind, such as new software for an experiment, start a separate
set with that kind and link it, as `BASE.md` says under "Linking
blueprint sets."
