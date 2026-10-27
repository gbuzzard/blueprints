# Kind: software

The design of a software project, written before any code.  This kind is
the Blueprinting starter kit, version 5 (C. A. Bouman), on the shared
base: the rules it shares with every kind are in `BASE.md`, and the rules
below are its own.

## 1. Product

Code, written from the settled blueprints.

## 2. Components

A set of blueprints is built from components.  Four core components cover
the design of almost any project.  Optional components cover other parts
that some projects need.  The person chooses which components their
project uses.  Each component answers one question a new developer asks.

**Core components**, in this order:

| Blueprint | The question it answers |
|---|---|
| 1. Theory | What is computed?  The quantities, grouped by kind, and the operations on them, with equations where they help. |
| 2. Software Architecture | What objects hold it?  The objects a user holds, every method of each, file formats, and which object holds each kind of quantity. |
| 3. Hardware Mapping | Where does it run?  What lives in host memory and in GPU memory, what each processor computes, and what moves between them, with sizes and times. |
| 4. User API | What does a user type?  The script a user writes for each use, and every public name. |

A core component may be left out when it does not apply, for example
Hardware Mapping for a program that runs on any computer.

**Optional components**, after the core ones:

| Blueprint | The question it answers |
|---|---|
| Pre and Post Processing | How does raw data get in and results get out?  Only load, save, import, and export functions touch files. |
| Testing and Verification | How do we know it is right?  The reference results the code must match, the tests, and what each test guards against. |
| Documentation | How does a new user learn it?  The pages, the examples, and where each public name is described. |
| Release and Maintenance | How does it reach users and stay current?  Packaging, the release steps, and any data that must be updated. |

The person may also name a component of their own.  Give it one question
it answers, in the same form.

**Front page.**  Keep all four core cards, in order.  A core component
the project does not need keeps its card, marked with the added status
label **not needed**, with one sentence saying why.  Under "Optional
components", keep the cards the person chose and delete the rest.  The
template is `kinds/software/templates/index.html`.

## 3. Tests and confusions

None in this version.

## 4. Interview

**Message 1**, after showing the example:

> This is the blueprinting kit.  It writes the design of your software as
> a few short web pages, called blueprints, before any code is written.
> Above is an example front page for a made-up project.
> Would you like me to start blueprints for your project?

**Message 3.**

> What is the project?  One or two sentences are enough.

**Message 4.**

> What should I read first: papers, code, data, or notes?  Tell me where
> they are, or say "nothing".

**Message 5.**  Look at what they pointed you to, then propose the
components yourself.  Do not show them a menu to choose from.  List the
core components that apply, any core one that is not needed with the
reason in a few words, and the optional ones this project needs, one
line each.  Then say:

> Is this the right set of blueprints?

Then set up the blueprint folder (Step 2 of `BASE.md`), open the front
page, and ask the person for input on the first component.

If research code exists, ask before running it.  Its outputs on fixed
inputs become the baselines the new code must match.

If the project changes existing code, read that code before writing the
Theory blueprint, and state the facts the design depends on as the code
has them.  A blueprint can also review existing code: its Theory then
describes what the code does now, followed by the open questions.

## 5. First draft

Write the User API blueprint by writing the script a user would run
first.  It is the cheapest thing to change.

## 6. Settling

Write the blueprints in order, one at a time.  Create each page from the
blueprint template when you start it, link it from the front page, and
mark it **for review** when the draft is ready.  Then show it, say what
to look at, and ask:

> Shall I go through the open questions with you now?

Do not start the next blueprint until this one is **settled**.

## 7. After settling

The blueprints change with the code.  From the first working version on,
a change to the code changes its blueprint in the same commit.

## 8. Execution

Write no code until every blueprint the project needs is settled.  Then:

1. Put `templates/CLAUDE.md` in the root of the project, as `BASE.md`
   Step 5 says.
2. Write the code from the blueprints.
3. Check it number for number against the baselines before changing any
   detail of the algorithm.
4. At the first working version, stop and walk through the names one at
   a time for clarity before any optimization.

When the project adds to existing code, extend its architecture.  Change
existing code only where the feature needs it, and put new code where it
logically belongs.

## 9. Outcome blueprints

None.  The code and its tests are the outcome.

## 10. Critique questions

- Is this correct?
- What will break?
- Is it easy to use?

## 11. Outside rules

None.

## 12. Links

An experiment's Plan may link a software set, when the experiment needs
new software.

## Other rules of this kind

- Propose the simplest design that meets the blueprints.  Add no feature,
  option, or safeguard that no blueprint asks for.
- Do not tie a design to one example case.  If a choice only fits the
  case at hand, say so.

## Example

`kinds/software/example/index.html` and `theory.html`: a made-up image
denoiser for a lab that scans samples on a benchtop microscope.
