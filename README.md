# Vibe64 learning catalogue

The initial owner is `mobily-enterprises`. This preview course selects two whole
topics, both grouped under the `vibe64` domain:

- `vibe64-getting-started` at release `0.5.0`;
- `vibe64-online-workspace` at release `0.1.0` (hosted Vibe64 only; Courses
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

The 0.5.0 lock pins `vibe64-getting-started` commit
`714b33d83cda7d05239f6d4162c70a3ca7edd03f` (manifest hash
`ef29094346f982c317bac2a750f726bbe73dfc36da5e37d47ef5360265ddf087`) and
`vibe64-online-workspace` commit `0bc2462ce835365377f8f37d24078ba88bbae498`
(manifest hash
`930f1ffae15ccdfeb860ed26cf8de87d2c15f9bd591131a35a51f40cafb25db9`). These are
the latest lesson commits whose text matches Vibe64 0.1.40 (lesson format 3,
the step bar's **Lesson** button). Later lesson commits describe the Lesson
toggle and the step bar's **Open practice project**, which ship with the next
Vibe64 release; pin them in a later course release once that is deployed.
They are the only releases listed in `topics.json`; earlier releases were
retired.

Installing 0.5.0 from Learning → Courses (**Install**, or **Update** from an
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
