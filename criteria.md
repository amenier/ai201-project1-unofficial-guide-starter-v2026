# Acceptance criteria — The Unofficial Guide

Five criteria that say what "working" means for this system, written in week 1
**before** any results existed.

An acceptance criterion names a target: a number, a count, a rate, or something
a person could plainly observe. *"Retrieval works"* is an opinion. *"For at
least 4 of my 5 test questions, the top results include a chunk containing the
answer"* is a criterion.

Under each one, write a sentence or two on **why that target** and not a
stricter or looser one. A reason that says something about your corpus or your
pipeline earns credit; *"80% seemed reasonable"* does not.

> Missing your own targets next week costs you nothing. Setting a target so
> easy you can't miss it does.

---

## 1. Retrieved chunks contain the answer

For at least 4 of my 5 test questions, the retrieved chunks include one that
contains the answer.

**Why this target:**

RAG systems are useless without good retrieval. Unless the retrieved chunks contain the answer, the system will not produce a useful result.

---

## 2. Every answer names a source

Every answer the system produces names at least one source document.

**Why this target:**

Naming the sources in the response provides traceability and credibility to the answers. The user can check the source to ensure that the answer is accurate and complete.

---

## 3. The relevance gate stops out-of-corpus questions

When I ask a question my documents clearly don't cover, the relevance gate
stops it and the system returns "I don't have enough information about that" —
in at least 4 of 5 tries.


**Why this target:**

A good RAG system refuses to answer questions that it cannot find a source for. Otherwise, the system can produce confidently incorrect answers that fool the user.

<!-- What did your distances look like when you set the cutoff in Milestone 4?
     Was there a clean gap, or did the two groups overlap? -->

---

## 4. Something about your chunks

The chunks retrieved will be contain complete sections separated by markdown headings.


**Why this target:**

The markdown headings in the city guides act as natural thought and topic separations. Because of this, I think the best approach is to preserve that organization in the chunks. This is also similar to many of the documents I will be using to build RAG systems at work: formal documents with clear headings.


---

## 5. Your choice

The system will return the paragraph number from the source document along with the document name.



**Why this target:**

The longer documents in this corpus make it difficult to evaluate the answer at a glance. By retrieving the paragraph number as well (with each markdown heading being considered a paragraph), the user will be able to find the source text more easily.

---

<!-- ─────────────────────────────────────────────────────────────────────────
     WEEK 2 — read this before you change anything above.

     If a criterion turns out to be BROKEN rather than merely unmet, you can
     revise it, and that earns credit. But never delete or edit the original
     line. Add the revision underneath it, like this:

         ## 1. Retrieved chunks contain the answer

         For at least 4 of my 5 test questions, the retrieved chunks include
         one that contains the answer.

         **Why this target:** ...

         > **Revised in week 2:** For at least 4 of 5 questions, the top three
         > results contain the answer.
         >
         > **Why revised:** I couldn't judge "the chunks include one that
         > contains the answer" the same way twice — I scored two questions
         > differently on Monday than on Wednesday. The new version is
         > something I can actually check.

     That's a revision because the criterion couldn't be MEASURED.

     Lowering a target because you missed it is not a revision, and it costs
     you the point:

         ✗ "I said 4 of 5 but got 2 of 5, so 2 of 5 is more realistic."

     A number you missed stays where it is, gets diagnosed, and gets a fix
     attempted. That's where the points are.

     The whole reason the originals stay visible is so someone can see what you
     said before you knew the answer.
     ───────────────────────────────────────────────────────────────────────── -->
