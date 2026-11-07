# Kind: paper

The design of a research paper, written before the manuscript and kept
with it until the paper is published.  The rules this kind shares with
every kind are in `BASE.md`, and the rules below are its own.

## 1. Product

A manuscript submitted to a venue, and later the response to its
reviews.

## 2. Components

Every paper has the same six blueprints, in this order.  Each answers
one question a reader asks.

| Blueprint | The question it answers |
|---|---|
| 1. Contribution | What does the paper show that was not known before? |
| 2. Significance | Who can use the result, and what can they do with it that they could not do before? |
| 3. Prior work | How does each claim differ from the closest published work? |
| 4. Methods | What was done, and which parts of it are new? |
| 5. Results | What supports each claim, and by how much? |
| 6. Outline | How is the paper organized, and where is it submitted? |

The first three blueprints are the **argument**: what the paper claims,
why it matters, and why it is new.  The last three are the **support**:
how the results were obtained, what they show, and how the paper
presents them.

Each blueprint has the sections below, in this order, followed by Open
questions and Decisions.  A section may be one line.  Write "None." in a
section that does not apply.

| Blueprint | Sections |
|---|---|
| Contribution | Claims: one to three, each one sentence, each naming the entry of the Results that supports it.  Not claimed: what a reader might expect the paper to show that it does not. |
| Significance | Readers: who can use the result.  What is new for them: for each claim, what a reader can now do, or do better, and by how much. |
| Prior work | Closest work: for each claim, the closest papers, what each shows, and how this paper differs.  Other related work: in groups, one line each. |
| Methods | Components: each component of the method, marked **new** or **standard**, with a citation for each standard one.  Data and experiments, or the setting and assumptions of each theorem.  Fair comparison: how each method's settings are chosen. |
| Results | For each claim: the theorem, figure, or table that supports it, its caption, and the number it gives against its comparison.  Objections: what a reviewer is likely to raise, each with its answer or an open question. |
| Outline | Venue: its name, format, page limit, and required sections, with the source document and its date.  Sections: one sentence each, with the figures and tables each holds.  Title and abstract, drafted from the front page. |

**Front page.**  Keep all six cards, in order.  Below the lead, write
"Submitted to VENUE on YYYY-MM-DD." or "Not yet submitted."  Once the
argument and the support are settled, the cards read in order as the
abstract: the claims, what they make possible, how they differ from
earlier work, how the results were obtained, and the numbers that
support them.  The template is `kinds/paper/templates/index.html`.

## 3. Tests and confusions

Apply these two tests to the claims and to the significance.

- **Contribution test.**  Each claim is one sentence that a reader could
  check against the paper.  It says what is new compared with the
  closest prior work, and an entry of the Results supports it.  A claim
  that a method is better says by how much, compared with what, and on
  which data.  No claim is broader than its results.
- **Significance test.**  The statement names who can use the result and
  what they can now do that they could not do before, or do much
  better.  It states that new capability plainly, at the start.  A
  statement fails if it names only the method's standard components or
  only why the field matters.

Three confusions are common.  Each comes from an abstract that the
owner of this kind reviewed.

| Confusion | Example | Follow-up question |
|---|---|---|
| Standard components presented as the contribution | "A method that achieves high-quality results by using a spectral decomposition and a spatial residual correction."  Both steps are standard. | "Which of these steps is new, and what does it let a reader do that they could not do before?" |
| The new capability left implicit or buried | An abstract on strain tomography that never says the method works in 3D, and names its mechanics constraint only inside a list of components. | "What does this method do that no earlier method does?  Can the first sentence say so?" |
| A comparative claim without a number | "Faster" or "accurate," with no amount and no comparison. | "Better than what, by how much, and on which data?" |

## 4. Interview

**Opening message**, after showing the example:

> This kit writes the design of your paper as six short web pages,
> called blueprints, before the manuscript is written: Contribution,
> Significance, Prior work, Methods, Results, and Outline.  Above is an
> example front page for a made-up paper.
> What is the paper about, and where do you plan to submit it?  What
> should I read first: drafts, results, code, or the papers it builds
> on?

After the front page is open, ask these two questions together, in one
message:

1. What does the paper show that was not known before?  One sentence
   per claim is enough.
2. Who can use these results, and what can they do with them that they
   could not do before?

The core statements are the claims and the significance.  After the
answers, apply the tests, check for the three confusions, and give your
view and proposed wording as `BASE.md` Step 3 says.  Ask again,
reworded, only about a statement that fails its test.

**Framing questions.**  In the next message, ask these five questions
together, and give your own answer to each, marked as a proposal, so
that the person responds to a proposal instead of starting from nothing:

1. Is this result a special case of a more general one?  What would the
   general statement be, and what would it cost to show it?
2. Who outside this application has the same problem, and would the
   method work for them?
3. Which component could be removed while keeping most of the gain?
4. Is there a simpler version of the problem, such as a linear,
   one-dimensional, or noise-free case, that shows the main idea more
   clearly?
5. If a reader remembers one sentence from the paper, what should it
   be?

Questions 1 and 2 look for a broader framing, and questions 3 and 4 for
a simpler one.  Ask about simplification explicitly, because people
more often add to a design than remove from it.  Think broadly about the
significance, but keep each claim as narrow as its results.  A broader
framing goes into the Significance, or into "Not claimed" on the
Contribution.  A simplification becomes an open question on the Methods
or the Contribution.

Draft the Prior work, Methods, Results, and Outline blueprints yourself,
from what you read, each with its open questions.  On Methods, mark each
component new or standard; when you cannot tell, make it an open
question.  Discuss the closest prior work with the person, who usually
knows it better than a search does.

## 5. First draft

Draft the Results first: for each claim, the figure or table that
supports it, with its caption.  Draw a planned figure as inline SVG,
with axes and units.  A result not yet in hand is a placeholder that
says what will go there, or a link to the experiment blueprints that
will produce it.  These are the cheapest items to change, and they show
at once whether each claim has support.

## 6. Settling

Settle the argument first, then the support.  The three blueprints of
the argument are settled together, because a claim is new only relative
to the prior work, and its significance depends on what it claims.  The
three blueprints of the support are settled together afterward, because
the claims decide what the paper must show.

Settling is a checkpoint, not a lock.  Results often arrive or change
while the paper is written, and the claims may need to change with
them.  Before its result is in, a claim is marked **expected** and holds a
placeholder for its number.  When a result arrives or changes, apply the
Contribution test again.  If a claim no longer passes, mark the argument **for review**, revise the
Contribution, the Significance, and the Prior work together, and settle
them again.  Record each change to a claim, with its date and reason, in
`decisions.md`.

Start the manuscript when both groups are settled, or earlier if the
person asks.  Then write on the front page what is not yet settled.

## 7. After settling

The blueprints change with the manuscript until it is submitted: a
change to a claim, a method, or a result in the manuscript changes its
blueprint at the same time.  At submission, write the venue and the date
on the front page, and keep the blueprints as submitted, as a copy of
the folder or as a commit, so that the reviews can be read against
them.

## 8. Execution

The manuscript is written from the settled blueprints, in the order of
the Outline, by the authors or by Claude when asked.  While it is
written, check that:

- each claim in the manuscript, including the abstract and the
  conclusion, is on the Contribution blueprint;
- each figure and table is on the Results blueprint, with the same
  caption;
- each component that the manuscript calls new is marked new on the
  Methods blueprint.

## 9. Outcome blueprints

When the reviews arrive, add a page `reviews.html` and link it from the
front page.  It holds the decision and each reviewer comment, numbered.
Each comment becomes an open question on the blueprint it concerns.  Put
these open questions to the person all at once.  Write the response to
the reviewers from the decisions, one answer per comment, naming the
change made in the manuscript.  A revised manuscript changes the
blueprints as section 7 says, and a new submission adds its venue and
date to the front page.

## 10. Critique questions

- Would a skeptical reviewer accept the result that supports each
  claim?
- Is any claim already in the prior work?
- Which claim is weakest, and would the paper be better without it?
- Does the first sentence of the abstract say what is new?
- Is there a shorter paper that makes the same contribution?
- The five framing questions of section 4.

## 11. Outside rules

The venue's author instructions set the format, the page limit, any
required sections, and often the review criteria.  Name that document
and its date on the Outline blueprint, and ask the person for the
current version instead of writing the rules from memory.  When the
venue publishes review criteria, give them to the critics too.

## 12. Links

A Results entry may link to an experiment's blueprints for a result not
yet in hand, and cite the experiment's Conclusion once it is settled.
Code released with the paper may be designed as a software set and
linked from the Methods.

## Other rules of this kind

- Propose the fewest claims that carry the paper.  A weak claim makes a
  reader doubt the strong ones.
- State each claim at the strength its results support.

## Example

`kinds/paper/example/index.html`, `contribution.html`, and
`methods.html`: a made-up report comparing a QGGMRF prior and a TV prior
in CT reconstruction, shown while its results are pending.
