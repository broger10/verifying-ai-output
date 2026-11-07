# Verifying AI output

How I make documents, analyses and decisions produced with AI systems checkable by someone else.

Method and examples by Andrea Brognera.

**In one line:** every claim carries its source. A declared share of those sources is reopened.
Whatever is still unverified is marked in the text, with the percentage.

> **What this method does not do.** It does not guarantee that the output is true. It makes the
> output traceable and checkable. A source can be reopened, confirmed, and still be wrong.

---

## The problem

AI systems write fluent text faster than anyone can reread it line by line. They make mistakes, and
the mistakes look exactly like the correct parts. A made-up quotation, a number the source does not
support, a "this is industry standard" with nothing behind it: all of them read well.

The question I work on: **when this document reaches a reader, can they tell which parts were
checked, against what, and which parts were not?**

---

## The seven rules

These rules stayed the same across three very different pieces of work.

1. **List the input and set the scope before producing anything.** Every part of the input is
   mapped or left out with a reason. Nothing drops out silently.
2. **Write the success criteria before the work, and keep them.** If the result fails a test, you fix
   the result, not the test.
3. **Every claim carries its source.** A claim without one is marked in the text, not in a footnote.
   The citation format is fixed in advance for each kind of source: document and section, timestamp
   in an audio file, screenshot number, web address with access date. A claim that is not in the
   source needs one of two things: a web source the reviewer opens, or a written derivation from
   something that is in the source. "Reasonable", "well known", "industry standard" and "obvious" do
   not count.
4. **Whoever produces does not approve.** Plan, work and review are done in separate AI agent
   sessions that share nothing but the written files. Each deliverable gets two independent checks.
   One looks for internal contradictions. The other reopens the sources one by one. They find
   different things.
5. **"Not found" is not "absent".** Before writing that something does not exist, show that the same
   search finds something you know is there.
6. **Contradictions are written down.** When two sources or two reviewers disagree, the disagreement
   stays in the record, with the decision and its reason. On facts about real people the method does
   not choose: it reports both versions and passes the question to the owner.
7. **The limits go out with the result.** A deliverable ends with what it did not check and where it
   could be wrong.

One more habit: every error found becomes a written rule, so the next piece of work does not repeat it.

---

## How a piece of work goes

1. **Brief.** Seven fields: goal, input, deliverable, success criteria, constraints, what is out of
   scope, and which decisions are reserved to the person who owns the work. If a field is empty or
   unclear, the questions go back to the owner in one batch before anything starts.
2. **Inventory of the input.** Large material is read in layers: structure first, then samples, full
   reading only inside the actual work. The step closes when every part is mapped or declared out of
   scope.
3. **Discussion before planning.** Each real decision gets two or three positions, the rejected
   alternatives and why, and a critic who looks for the weak points. Decisions that belong to the
   owner are collected, each with a recommendation.
4. **Acceptance tests first.** The final tests (input and expected result) are written from the
   success criteria, before any work is done.
5. **Small, self-contained units of work.** Each unit must pass the "fresh session" test: someone
   with no memory of the project can carry it out from that unit and the documents it points to.
   State lives in files, never in "I remember".
6. **Two checks before each unit runs.** A stress test of the plan, and a check that every reference
   in the plan says what the plan claims. Both must pass, or the unit does not start.
7. **Execution.** If an assumption stops holding, the work stops. The problem is written down and the
   unit goes back to the two checks. Nobody improvises outside the plan.
8. **Final test by a reviewer who sees only the result.** Failures go into a gap list and get a
   targeted fix. Only the failed tests are run again.

**What stays with a person:** pricing, brand, positioning, facts about real people, and anything
irreversible. Where there is a client, "delivered" does not mean "sent": the final message goes to
the owner, who decides whether to send it.

A one-page version is in [`CHECKLIST.md`](CHECKLIST.md). A blank brief and review record is in
[`TEMPLATE.md`](TEMPLATE.md).

---

## What it does not guarantee

- Traceable is not true. In one case a range presented as "industry standard" really was in the
  source, and was false. Reopening the source confirmed the citation, not the fact.
- Not every source is reopened. In the largest case, 86 quotations were extracted and 17 were reopened
  against the source; 3 of those did not hold. 72 of 85 web addresses were opened. That is a declared
  sample, not a full check: 69 quotations were never reopened.
- The "unanchored" percentage measures marking, not accuracy. 15.0% of the content was marked as not
  traceable to the source. That says nothing about the other 85%, and only a minority of it was
  reopened. A document with honest markings can still be wrong.
- Separate roles are separate sessions, not separate people. When the same AI system writes and
  reviews, the review is not an independent second opinion. Nobody has measured the difference.
- Drift between documents gets through. The checks compare claims against the world, not documents
  against each other. It happened in all three cases: a count that differed across three files, a
  file that misstated its own length, a cross-reference to a section that did not exist. No check
  caught it. The checklist now has a manual step for it.
- The final test can miss the worst defect. In one case the most serious design flaw was confirmed
  because the final test did not fail on it.
- It measures activity, not effectiveness. The numbers show that the method finds defects. They do
  not show how many remain, and there is no comparison with the same work done without it.
- The evidence for the method was produced with the method. The case write-ups use the approach they
  describe, and part of the evidence on the first case is second-hand, as the analyst declared.
- None of the three cases was paid work for a third party. They were done on my own archive and my
  own products. That is also why I can show everything, including what went wrong.
- It has a fixed cost. Where a mistake is cheap, this is more process than the work deserves. It also
  needs a real test surface: in one case, testing on demo data proved nothing because the demo data
  was already correct.
- It does not cover value decisions. Those go to the owner and stay open.

---

## Three cases

All three are anonymized.

**A · Turning an academic archive into usable documents.** 316,935 files (6.3 GB) reduced to 1,160
that mattered, then to 15 documents that someone else can use without opening the source. Each
document had two independent checks. The checks sent documents back five times across four
documents, one of them twice in a row. Reopening the sources found two quotations that did not exist
anywhere in the source, inside the very document that taught how to distrust quotations.

**B · Four minutes of voice notes from a pilot user of a live product.** Every piece of material
received (audio, screenshots, a spreadsheet) was mapped to a fix or declared not actionable. The
cause was measured in the data instead of argued from the screen. A separate reviewer challenged the
first diagnosis and corrected it. Five hours after delivery the product broke again for a different
reason. It was fixed the next day with a cost model fitted on five real measurements (0.2% error),
not by guessing a new limit.

**C · Building the knowledge base of an AI product before it exists.** There is no product to test
here, so the check moves to the sources the product will be built on, with a different standard of
proof for each kind of claim. Twelve of sixteen real user messages, from five people, asked for
exactly what the product must not give. The research itself calls the sample small. The design
followed from it. The drift between documents showed up here too: one list counted as 15, 20 and 19
in three files that cite each other.

---

## What is borrowed, and what is mine

Most of the pieces are standard practice under other names: the four-eyes principle, acceptance
criteria written first, decision records with rejected alternatives, source and year for every
number, positive controls before declaring something absent, "citation needed" marked inline, and
groundedness or attribution rate in AI evaluation.

What I add:

- putting them together on AI-produced work, with roles split across separate sessions and files
  instead of memory;
- a threshold on unanchored content per document: above 30%, the owner is told;
- a written rule for when the word limit and the markings conflict: cut content, keep the markings;
- treating words like "only", "first" and "none" as claims to prove, not adjectives;
- applying all of it to my own work, and showing where it did not hold.

---

*Andrea Brognera*
