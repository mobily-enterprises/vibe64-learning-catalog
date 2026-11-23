# Vibe64 learning catalogue

The initial owner is `mobily-enterprises`. This preview course selects two whole
topics, both grouped under the `vibe64` domain:

- `vibe64-getting-started` at release `0.5.2`;
- `vibe64-online-workspace` at release `0.1.5` (hosted Vibe64 only; Courses
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
| V64-WORKSPACE-01 to 05 | Your hosted Vibe64 workspace (five studio lessons; three publish the sign app for real from the Deploy page) |

Lessons 0–3 each create a practice project, an ordinary project marked as
practice that the learner can delete with one click.

The 0.5.4 lock pins `vibe64-getting-started` commit
`44a2fee535ef0f91f1b148cbad33c61ba0355665` (manifest hash
`c5b32d59ac4b8e5c336a7bd138f56be6950cb06d532ba5504e98c4b6d99aac70`) and
`vibe64-online-workspace` commit `6496576a845738576f11d813dc1b862d8a24e694`
(manifest hash
`c12080d78cab77d2a23a76e543fa36cfe529be60fa3112c3d742def7a5e1bdb0`). Their text
matches the deployed Vibe64: lesson format 3, the **Lesson** toggle that covers
Preview or Dash, the step bar's labelled **Back** / **Next** and **Open practice
project**, a lesson pane without Previous/Next step links, and the hosted
**Deploy** page (Dashboard → Deploy) with **Publish to staging** for the Staging
environment (its Test addresses, Staging address and Staging releases, and an
app running on Staging, under the names hosted Vibe64 gives them since 20 Nov),
the Production card's **Publish to production**, **Test copy** and
**Switch to Live**. They are the only releases listed in `topics.json`; earlier
releases were retired.

Installing 0.5.4 from Learning → Courses (**Install**, or **Update** from an
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
