# Vibe64 learning catalogue

The initial owner is `mobily-enterprises`. This preview course selects two whole
topics, both grouped under the `vibe64` domain:

- `vibe64-getting-started` at release `0.5.1`;
- `vibe64-online-workspace` at release `0.1.1` (hosted Vibe64 only; Courses
  leaves these lessons out where their screens do not exist).

Every lesson uses lesson format 3: short steps the learner reads in the
Learning environment (**L**) without needing AI, on a stage (`studio` for a
lesson about the studio pages, `project` for one with a practice project).
**Teach me** asks Colleague to explain the current step on the real screens and
**Show me** points at the place a step talks about. The yellow lesson step bar
plays steps as short guided beats. Colleague never grades: a step passes only
through an automatic check, a fact check, a choice question compared on the
server, a review of the learner's practice changes by their own AI against the
step's rubric (run only when the learner presses **Check my work**), or the
learner's own **Done**. Each lesson has learner-facing **Lesson notes**.

| Code | Lesson |
| --- | --- |
| V64-WELCOME | Welcome to Vibe64 (studio orientation; **Take the tour** starts it) |
| V64-START-00 | Introduction to the editor (practice project: tour app) |
| V64-START-01 | Your first steps in Vibe64 (Preview press checked automatically) |
| V64-START-02 | Make your first change (code check on `greeting.mjs`; requires 01) |
| V64-START-03 | Build with a database (SQLite notes app; requires 01) |
| V64-WORKSPACE-01 to 05 | Your hosted Vibe64 workspace (five studio lessons; three deploy the sign app for real) |

Lessons 0–3 each create a practice project, an ordinary project marked as
practice that the learner can delete with one click.

The 0.5.1 lock pins `vibe64-getting-started` commit
`2ff61fd3f31c7453e79d2a5b63aaeb5922b9f803` (manifest hash
`35e2e71888b897274c897e8c8ab479e7e696eb8f80e0d45c3875dbab220c701c`) and
`vibe64-online-workspace` commit `e180238dfd9ed2f463b0960bc027f6b72896a6b7`
(manifest hash
`683284bc874d64ae12f89135aee9c174a1c4d146708109c857b767e160929c41`). Their text
matches the deployed Vibe64: lesson format 3, the **Lesson** toggle that covers
Preview or Dash, the step bar's labelled **Back** / **Next** and **Open practice
project**, and a lesson pane without Previous/Next step links. They are the only
releases listed in `topics.json`; earlier releases were retired.

Installing 0.5.1 from Learning → Courses (**Install**, or **Update** from an
earlier release) enables it and disables older enabled releases of the same
course for new starts only; installed learner pins remain intact. Because it is
a preview, only the workspace owner can start its lessons, with **Try preview**;
members see it but can start it only once a released course is published.
Real learner acceptance remains open.

Courses select whole topic releases. Do not add lesson selections to a course or
hand-edit a lock to omit or reorder a topic's lessons.

Generate the reviewed local lock with the installed Vibe64 authoring command:

```sh
vibe64 training publish-manifest courses/getting-started-with-vibe64/course.json ../learn-vibe64-getting-started ../learn-vibe64-online-workspace
```

Each topic must be a clean checkout of its pinned commit. The
command verifies every hashed input against the exact Git commit and writes
`course.lock.json` atomically. It does not create a remote release. Repository
publication follows the normal reviewed Git workflow. Installation and enabling
a topic remain owner-authorised application operations, with learner access
checked separately. Existing attempts can continue pinned content after a release
is disabled; new starts are blocked.

The lock includes repository, immutable commit, manifest hash and every ordered
lesson identity. A released course requires released topics with no required drafts.
Review learner outcomes and complete every lesson with real learners before release.
