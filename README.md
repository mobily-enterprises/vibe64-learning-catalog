# Vibe64 learning catalogue

The initial owner is `mobily-enterprises`. This preview selects the entire
`vibe64-getting-started` topic at release `0.4.2`, grouped under the `vibe64`
domain. It is a Learning v2 release: every lesson uses lesson format v2,
a list of short steps the learner reads in the Learning environment (**L**)
without needing AI. **Teach me** asks Colleague to explain the current step on
the real screens and **Show me** points at the place a step talks about.
In Lesson 0 the yellow lesson step bar also plays each step as short guided
beats. Colleague never grades: a step passes only through an automatic check, a
choice question compared on the server, a review of the learner's practice
changes by their own AI against the step's rubric (run only when the learner
presses **Check my work**), or the learner's own **Done**. Each lesson has
learner-facing **Lesson notes**.

| Code | Lesson |
| --- | --- |
| V64-START-00 | Introduction to Vibe64 (practice project: tour app; a guided tour of the editor) |
| V64-START-01 | Your first steps in Vibe64 (Preview press checked automatically) |
| V64-START-02 | Make your first change (code check on `greeting.mjs`; requires 01) |
| V64-START-03 | Build with a database (SQLite notes app; requires 01) |

Lessons 0–3 each create a practice project, an ordinary project marked as
practice that the learner can delete with one click.

The 0.4.2 manifest and generated lock pin topic commit
`1c96ec2f8c1e4cd4b995cb77c91f368df1082760` (manifest hash
`8e02b90d212adab4d443e84fd27f870df25264387daa290b18058f95680fa2a6`). It is the
only release listed in `topics.json`; earlier releases were retired. Lesson 0
introduces the editor on a minimal practice project, and the lesson step bar
plays its steps as guided beats: it points at each part of the editor, notices
when the learner does what a line asks and marks such steps done. Its first
change is passed with **Check my work**: the learner's own AI reviews the
practice project's changes against the step's rubric. AI setup is not a lesson.

Installing 0.4.2 from Learning → Courses (**Install**, or **Update** from an
earlier release) enables it and disables older enabled releases of the same
course for new starts only; installed learner pins remain intact. Because it is
a preview, only the workspace owner can start its lessons, with **Try preview**;
members see it but can start it only once a released course is published.
Real learner acceptance remains open.

Courses select whole topic releases. Do not add lesson selections to a course or
hand-edit a lock to omit or reorder a topic's lessons.

Generate the reviewed local lock with the installed Vibe64 authoring command:

```sh
vibe64 training publish-manifest courses/getting-started-with-vibe64/course.json ../learn-vibe64-getting-started
```

The topic must be committed and clean on its canonical `main` checkout. The
command verifies every hashed input against the exact Git commit and writes
`course.lock.json` atomically. It does not create a remote release. Repository
publication follows the normal reviewed Git workflow. Installation and enabling
a topic remain owner-authorised application operations, with learner access
checked separately. Existing attempts can continue pinned content after a release
is disabled; new starts are blocked.

The lock includes repository, immutable commit, manifest hash and every ordered
lesson identity. A released course requires released topics with no required drafts.
Review learner outcomes and complete all four lessons with real learners before release.
