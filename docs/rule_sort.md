# Where each rule of the two earlier kits went

This kit was made from two kits: the Blueprinting starter kit, version 5
(called v5 below), and the experiment blueprinting kit, version 3 (called
E3 below).  Each rule of either kit went to `BASE.md` when both kits share
it or every kind needs it, and to a kind file when only one kind needs
it.  The table lists every rule, where it is now, and any change.

## Changes to the software kind's behavior

The software kind behaves as v5 does, except for six changes:

1. Questions end without bracketed answers, such as "[yes / no]", as
   Greg decided for the experiment kit on 2026-10-24.
2. Before the first blueprint is settled, Claude asks once whether an
   advisor or a collaborator should review the design.
3. A step not yet done gets a placeholder that says what will go there,
   never an invented result.
4. Equations are written in MathML, as Greg's proposal for v6 says.
5. The skill is installed as `/blueprints` instead of `/blueprinting`,
   so it does not replace an installed copy of v5.
6. The person's own words come first on a kind's core statements.  The
   software kind has no core statements yet, so this changes nothing in
   practice.

## The rules

| Rule | v5 | E3 | Now in | Change |
|---|---|---|---|---|
| Safety rules 1, 3, and 4 | Yes | Yes | `BASE.md` | None. |
| Safety rule 2: ask before a command, an install, the network, a commit, or a push | Yes | Adds "start any run" | `BASE.md` | Both lists joined. |
| The blueprints are the record of the design | "The only channel between the person's intent and your implementation" | "The record of the experiment" | `BASE.md` | Worded for any kind. |
| The components and the question each answers | Menu: four core, four optional, or the person's own | Fixed: five | Kind files, section 2 | None. |
| Status labels | Adds **not needed** | Adds **running** | `BASE.md` has four; kinds add theirs | None. |
| Step 1 messages | Five messages, with bracketed answers | Four messages | `BASE.md` gives the order; kind files give the words | Brackets dropped. |
| How to show a page | Yes | Yes | `BASE.md` | Brackets dropped. |
| How to ask | One question, answers in brackets | One question | `BASE.md` | Brackets dropped. |
| Read what the person pointed to; ask before running code | Yes | Yes | `BASE.md` Step 1 | None. |
| Research code outputs become baselines; read existing code before Theory; a blueprint can review existing code | Yes | No | Software, section 4 | None. |
| Set up the folder; open the front page at once | Yes | Yes | `BASE.md` Step 2; front page rules in kind files | None. |
| Propose the components, then ask whether the set is right | Message 5 | No | Software, section 4 | Brackets dropped. |
| Interview questions 1 to 6; sort the first answer into Goal, Motivation, and Plan | No | Yes | Experiment, section 4 | None. |
| Goal test, Motivation test, and four confusions | No | Yes | Experiment, section 3 | None. |
| Own words first, critique in one or two sentences, wording only on request | No | Yes | `BASE.md` Step 3 | Now applies to every kind's core statements. |
| Draft first the item cheapest to change | The User API script | The planned figures | `BASE.md` Step 3; kind files, section 5 | None. |
| Page rules: only what will be built, the person's terms, the best form, one screen, open questions with checkboxes, the decided chip | Step 3 | Template and Step 5 | `BASE.md` Step 3 | MathML added. |
| Each missing fact becomes an open question with a recommendation | Implied | Step 4 | `BASE.md` Step 3 | None. |
| A placeholder for a step not yet done | No | From the TV example | `BASE.md` Step 3 | New. |
| One blueprint at a time; the next starts after this one is settled | Yes | No | Software, section 6 | Brackets dropped. |
| Design drafted together and settled together on one date | No | Yes | Experiment, section 6 | None. |
| Settings, Search, return to an earlier blueprint, pilot runs | No | Step 4 | Experiment, section 6 | None. |
| Review: read as a reader would, independent critique, findings, one question at a time, revise, shorten | Step 4 | Step 5 | `BASE.md` Step 4 | None. |
| Critique questions | Three | Five | Kind files, section 10 | None. |
| Share the folder with a collaborator | A sentence in Step 4 | The reviewer question | `BASE.md` Step 4 | The reviewer question now applies to every kind. |
| CLAUDE.md in the project root when the work needs code | Yes | Yes | `BASE.md` Step 5 | None. |
| No code before the blueprints are settled; code from the blueprints; match baselines number for number; walk through the names | Step 5 | No | Software, section 8 | None. |
| Extend the existing architecture; change existing code only where needed | Step 3 | No | Software, section 8 | None. |
| A code change changes its blueprint in the same commit | Step 5 | No | Software, section 7 | None. |
| Fixed record after settling; changes are dated deviations | No | Yes | `BASE.md` Step 5 states the rule; Experiment, section 7 uses it | None. |
| Ask before runs; reproduce the baseline; run checks; records; the running label | No | Step 6 | Experiment, section 8 | None. |
| Measured results, three questions, the Conclusion | No | Step 7 | Experiment, section 9 | None. |
| A next experiment cites this Conclusion | No | Yes | `BASE.md` Step 6; Experiment, section 12 | Worded for any kind. |
| An experiment that needs software links a software set | No | Yes | `BASE.md` "Linking blueprint sets" | Worded for any kind. |
| Less is more | Yes | Yes | `BASE.md` | The two lists joined; each kind keeps its own "smallest design" rule. |
| Ask only the listed questions | "The three interview questions" | "The questions in this file" | `BASE.md` | "In this file and in the kind file." |
| How to write | Yes | Yes | `BASE.md` | The last rules of each kit joined as "Do not generalize from one case"; each kind keeps its own wording too. |
| Report measurements on the Results; the Conclusion records the interpretation | No | Yes | Experiment, other rules | None. |
| How to write math (MathML) | Proposed for v6 | Yes | `BASE.md` | None. |
| Templates | Front page, blueprint, decisions, CLAUDE.md | The same four, written for experiments | `templates/` holds generic ones; software replaces the front page; experiment replaces the front page and the blueprint page | The v5 blueprint template gains the MathML rules and example. |
| Examples | Image denoiser: front page and Theory | CT denoisers: front page, Motivation, and Plan | `kinds/<kind>/example/` | The Theory page's equations are in MathML. |
