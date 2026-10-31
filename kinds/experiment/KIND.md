# Kind: experiment

The design of a computational experiment, written before any run, and the
record of its results and conclusion afterward.  This kind is the
experiment blueprinting kit, version 3, on the shared base: the rules it
shares with every kind are in `BASE.md`, and the rules below are its own.

## 1. Product

Measured results and a conclusion: the experiment's result and the
action it leads to.

## 2. Components

Every experiment has the same five blueprints, in this order.  Each
answers one question a reader asks.

| Blueprint | The question it answers |
|---|---|
| 1. Goal | What will the experiment measure or determine? |
| 2. Motivation | What will we do differently depending on the result? |
| 3. Plan | How will the runs measure it, and at what cost? |
| 4. Results | What did we predict, and what did we measure? |
| 5. Conclusion | What is the result, and what do we do next? |

The Goal, the Motivation, the Plan, and the Planned section of the
Results are the **design**.  The Measured section of the Results and the
Conclusion are written after the runs.

Two definitions keep the Goal and the Motivation apart:

- The **Goal** is what the experiment will measure or determine.  It
  may be written as a statement, such as "Measure how much ...", or as a
  question.
- The **Motivation** is the decision or next step that the result
  changes.  Write it as a statement of the decision, such as "Decide
  whether ...", not as a question.

Each blueprint has the sections below, in this order, followed by Open
questions and Decisions.  A section may be one line.  Write "None." in a
section that does not apply.

| Blueprint | Sections |
|---|---|
| Goal | Statement.  Quantity, data, and baseline: the quantity measured, any other quantities that must not get worse, the data, and the method or setting the experiment compares against.  Out of scope. |
| Motivation | Decision: what will be decided, and who decides.  What is known now.  Outcome table. |
| Plan | Runs: the baseline run, what is varied and over what values, and what is held fixed.  Fair comparison: what must match for two runs to be compared, how it is matched, and how each method's settings are chosen (see section 6).  Metrics: each score, defined.  Run checks: how each run is shown to have worked before it is scored.  Repeats: how many, and the run-to-run variation expected.  Search: the stages, the pruning rule, and the limits (see section 6).  Budget: compute time, calendar time, and the stopping rule.  Pilot runs: each with the open question it settles.  Records: what is saved for each run.  Deviations: added only after the design is settled. |
| Results | Planned: each figure and table, with axes and units, the predicted outcome and the reason for it, and how each row of the outcome table would appear in it.  Measured: added after the runs. |
| Conclusion | Result: one sentence.  Outcome: the row of the outcome table that occurred, and its action.  Surprises.  Undetermined.  Next experiment. |

The **outcome table** on the Motivation blueprint has one row for each
possible result of the Goal, and two columns: the result, and the action
it leads to.  The rows cover every possible result, including "no
difference."  When the experiment scores several images or data
sets, or several quantities, include rows for results that differ across
the data and for a gain in the main quantity with a loss in another; one
row may cover both.  A row may name a judgment instead of a number, such
as "much lower noise," if it says what the judgment weighs.  An action
may be a discussion, if the row says what the discussion decides.

**Front page.**  Keep all five cards, in order.  Below the lead, write
"Design settled on YYYY-MM-DD." or "Design not yet settled.", and the
reviewer's name or "none."  Once the design is settled, the front page
reads as the five entries of the experiment, filled in.  The added
status label **running** is used
only on the Results card, between the settled design and the measured
results.  The templates are `kinds/experiment/templates/index.html` and
`blueprint.html`.

## 3. Tests and confusions

Apply these two tests to every Goal and Motivation statement.

- **Goal test.**  The Goal names the quantity measured, the data, and,
  for a comparison, the baseline.  Its result is a number, a curve, a
  comparison, or a yes or no, so a third person could tell after the
  runs whether the Goal was met.  The data are like the data
  the decision applies to, because a method can score well on test data
  that favor it and poorly on the data it will be used on.
- **Motivation test.**  At least two rows of the outcome table lead to
  different actions.  If every result leads to the same action, the
  experiment gives no actionable information.  An exploratory experiment
  passes when its outcome changes what the next experiment studies.

Four confusions are common.

| Confusion | Example | Follow-up question |
|---|---|---|
| A step of the plan stated as the Goal | "Run a learned denoiser in the reconstruction loop." | "That is a step of the plan.  What would that step measure?" |
| A broad aim stated as the Goal | "Improve image quality." | "No single experiment can show that.  What part of it can this experiment measure?" |
| The Goal restated as the Motivation | "To find out whether the noise goes down." | "That restates the Goal.  What would you do with the result?" |
| The field's importance stated as the Motivation | "Lower dose matters for patients." | "That says why the field matters.  What decision does this result change?" |

## 4. Interview

**Message 1**, after showing the example:

> This is the blueprinting kit.  It writes the design of your experiment
> as five short web pages, called blueprints, before any run: Goal,
> Motivation, Plan, Results, and Conclusion.  Above is an example front
> page for a made-up experiment.
> Would you like me to start blueprints for your experiment?

**Message 3.**

> What experiment do you want to do?  One or two sentences are enough.

**Message 4.**

> What should I read first: papers, code, data, earlier results, or
> notes?  Tell me where they are, or say "nothing".

After the front page is open, sort the answer to Message 3 into Goal,
Motivation, and Plan, in the person's words, and show the sort as a short
list.  Say which of the three is missing.  Then ask these questions, one
per message:

1. What will the experiment measure or determine?
2. Suppose you had the result today.  What would you do differently
   because of it?
3. What are the possible results, and what would you do after each one?
4. What figure or table would show the result?
5. What do you expect it to show, and why?
6. What result would count as clearly better and as clearly worse, in
   numbers if you can?

The core statements are the Goal and the Motivation.  After each answer
to questions 1 to 3, apply the tests and check for the four confusions,
and give your view and proposed wording as `BASE.md` Step 3 says.  Ask
questions 1 to 3 again, reworded, until both tests pass.  Discuss earlier
experiments as they relate to this one, and check any value the design
takes from an earlier run against that run's record.  If the
Motivation test fails, say:

> Every result leads to the same next step, so the experiment would not
> change what you do.  Shall we change the Goal, or is there a
> decision I missed?

Then write the Goal and Motivation blueprints and the Planned section of
the Results from the answers.  Build the outcome table from the answers
to questions 3 and 6.

## 5. First draft

Write the Planned section of the Results by drawing the figures first,
as inline SVG with axes, units, and the predicted curves drawn dashed.  A
sketched figure is the cheapest thing to change, and it makes the Goal
name a measured quantity.

When both methods run on the same images or noise realizations, plan
paired comparisons: for each quantity, a scatter plot of the new
method's score against the baseline's, one point per image, with the
line of equality, and the mean and standard deviation of the per-image
differences or ratios.  Choose any example images by a rule fixed before
the runs, such as the images with the smallest, median, and largest
ratio, and show both methods with the same display range.

## 6. Settling

The four design blueprints limit one another, so you draft them
together, and the person settles them together, on one date, before any
run.

**Draft the Plan** from what you read and the answers so far.  Draft
each section yourself.  Define each metric in words, and also by an
equation in MathML when an equation states it more exactly.  Discuss
contingency plans with the person as needed.

**Settings.**  Choose each method's settings the way they would be chosen
in use, on data not used for scoring.  A comparison is unfair if the new
method is tuned and the baseline is left at a poor setting.

**Search.**  When the Plan varies several settings, or one setting over
a wide range, propose a limited tree search instead of running every
combination.  The runs then go in stages, and poor settings are dropped
after each stage.  The Search section states:

- the first stage: the settings run first;
- the pruning rule: the measured result that drops a setting, such as a
  failed run check, or a score worse than the best one by more than the
  run-to-run variation;
- the next stage: the new settings that each kept setting leads to, such
  as settings halfway to its neighbors;
- the limits: the largest number of stages and the largest number of
  runs;
- the end: when the search stops, such as when one setting beats every
  other by more than the run-to-run variation, or when a limit is
  reached.

Pruning that follows the settled rule is part of the Plan, not a
deviation.  Score the best setting again on data or noise realizations
not used to choose it, because the best of many runs scores high partly
by chance.  The Planned section of the Results then shows a table of the
stages, with each setting kept or dropped, and the final comparison of
the best setting with the baseline.

**Return to an earlier blueprint** when one of these tests fails:

- The Motivation test fails: every possible result leads to the same
  action.  Change the Goal, or drop the experiment.
- The Plan cannot meet the Goal within the budget.  Narrow the Goal,
  or raise the budget if the Motivation justifies the cost.
- The predicted difference is smaller than the run-to-run variation, so
  the planned figures cannot tell the outcomes apart.  Change the Plan,
  for example with more repeats or another metric, or change the Goal.
- A pilot run shows that the setup does not work.  Change the Plan.

**Pilot runs.**  Make a pilot run only to settle an open question that
the Pilot runs section names.  Ask before each one, and record its
result there.  Make no other runs before the design is settled, unless
the person asks to start them early.  Then write on the front page what
is not yet settled, and fix the predictions, in the Planned section of
the Results or in the code that computes them, before any measurement is
read.

**Settle.**  When the open questions on the design are decided, and after
the reviewer question of `BASE.md` Step 4, ask:

> Shall I mark the design settled today?

With a yes, mark the Goal, Motivation, Plan, and Results cards
**settled**, and write the date on the front page.

## 7. After settling

The design is a fixed record: change no settled text.  A change to the
Plan is a deviation, as `BASE.md` Step 5 says, and goes in the Plan's
Deviations section.

## 8. Execution

1. Ask before the runs start, and once before each stage of a search.
2. Reproduce the baseline result first.  If it does not match the
   earlier result, stop and tell the person.
3. Check each run with the Plan's run checks before you score it.  A run
   that fails its check is recorded, labeled, and kept out of the
   comparison.  Its scores may be reported to show the size of the
   failure.
4. Record each run as the Records section says.
5. Mark the Results card **running**.

## 9. Outcome blueprints

1. Write the Measured section of the Results: the same figures and
   tables as planned, with the measurements beside the prediction:
   measured curves solid, next to the dashed predicted ones.  Label any
   figure that was not planned "not planned."  Define each series where
   it is reported, give every table of a series the same rows, and list
   only the final runs in a summary.
2. Ask these questions, one per message:

   > Which row of the outcome table occurred?

   > What surprised you?

   > What remains undetermined?

   If no row occurred, the outcome table missed a case.  Say so on the
   Conclusion blueprint.
3. Write the Conclusion from the answers, mark the Results and the
   Conclusion **for review**, and show them.  If the design had a
   reviewer, offer to send both pages to the same reviewer.
4. Put any open questions to the person one at a time.  Then mark the
   Results and the Conclusion **settled**.

A next experiment starts a new blueprint folder.  Its Motivation cites
this Conclusion.

## 10. Critique questions

- Does the Plan measure what the Goal names?
- Can any outcome change the decision?
- What would make the comparison unfair?
- Is the predicted difference larger than the run-to-run variation?
- Is there a cheaper experiment that meets the same Goal?

## 11. Outside rules

None.

## 12. Links

If the experiment needs new software, design the software as its own set
with the software kind, and link it from the Plan.  A later experiment's
Motivation cites this experiment's Conclusion.

## Other rules of this kind

- Propose the smallest experiment that meets the Goal.  Add no run,
  setting, or metric that the Goal does not need.
- Report measurements on the Results blueprint.  Let the person interpret
  them; the Conclusion records their interpretation.

## Example

`kinds/experiment/example/index.html`, `motivation.html`, and
`plan.html`: a made-up comparison of a Gaussian denoiser and a TV
denoiser in CT reconstruction, shown while the design is under review
and one pilot run is pending.
