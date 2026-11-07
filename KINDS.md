# How a kind is defined

A **kind** is one type of work that can be blueprinted, such as software
or a computational experiment.  Every kind follows `BASE.md`.  A kind adds
only what differs from one type of work to another.

## The folder of a kind

| Path | What it holds |
|---|---|
| `kinds/<kind>/KIND.md` | The kind file: its answers to the twelve questions below, and any rules of its own. |
| `kinds/<kind>/example/` | A made-up front page and one or two filled-in blueprints.  Claude shows the front page first. |
| `kinds/<kind>/templates/` | Optional.  A template here replaces the file of the same name in `templates/` for this kind. |

## The twelve questions a kind file answers

Each question is a numbered section of the kind file, in this order.
Write "None." in a section that does not apply.

1. **Product.**  What does the work produce?
2. **Components.**  Which blueprints does a set have?  Are they fixed, or
   chosen from a menu?  What reader's question does each answer, and
   which sections does each page have?  What does the front page show,
   and which status labels does the kind add?
3. **Tests and confusions.**  Which statements are the core statements,
   what test must each pass, and which confusions are common, each with
   a follow-up question?
4. **Interview.**  The exact words of the opening message of `BASE.md`
   Step 1, any messages the kind adds, and the questions that draw out
   the core statements.
5. **First draft.**  Which item is drafted first, because it is the
   cheapest to change?
6. **Settling.**  Are the blueprints drafted and settled one at a time,
   or together?  Which blueprints must be settled before the work starts?
7. **After settling.**  Do the blueprints change with the work, or do
   they stay a fixed record with dated deviations?
8. **Execution.**  What is made from the settled blueprints, and what is
   checked while it is made?
9. **Outcome blueprints.**  Which blueprints, if any, are written after
   the work, and from which questions?
10. **Critique questions.**  What is an independent critic asked?
11. **Outside rules.**  Which requirements come from outside the
    person's group, such as a funding agency's required sections, page
    limits, and review criteria, or a journal's format?
12. **Links.**  Which other kinds may a blueprint of this kind link to or
    cite?

After the twelve sections, a kind file may add a section "Other rules
of this kind" and must end with a section "Example" that names its
example pages.

## Adding a kind

A new kind has an **owner**: a person who has done this type of work
many times and who answers the questions about it.

1. Write a short proposal for the kind, and agree on it with the owner
   before writing the kind file.  The proposal names:
   - the components, and the reader's question each one answers;
   - the core statements;
   - the three choices on which the existing kinds differ: fixed or menu
     components (question 2), blueprints settled together or one at a
     time (question 6), and pages that change with the work or a fixed
     record (question 7).
2. Ask the owner for weak core statements from real cases, such as
   proposals or papers they have reviewed.  Write the kind's tests and
   confusions (question 3) from these cases.
3. Copy the folder of the existing kind that is closest to the new one.
4. Answer the twelve questions in its `KIND.md`.  Keep a rule in the kind
   file only when it differs from `BASE.md` or adds to it.
5. Write a made-up example: a front page and one or two blueprints.
6. Run the kind's interview on the made-up example, with Claude asking
   the questions and the owner answering them.  Revise the kind file
   where the run shows a rule that is missing or unclear.
7. Try the kind on a real piece of work, with its author as the person,
   before anyone else uses it.  A real case shows what the kind file
   lacks.
8. Add the kind to the list in `SKILL.md` and to the list of kinds at the top of the human part of `README.md`.

## Rules for changing the kit

- **Change `BASE.md` only for a rule that every kind needs.**  A rule
  that only one kind needs stays in that kind's file.  Before a change to
  `BASE.md` is committed, check it against each existing kind file and
  its example, and record it, with its date and its reason, in
  `docs/rule_sort.md`.
- **Cite outside rules from their source.**  Outside rules, such as a
  funding agency's required sections and page limits, change from year
  to year.  In section 11, name the source document and its date, and
  tell Claude to ask the person for the current version instead of
  writing the rules from memory.
