# Vibe64 learning catalogue

The initial owner is `mobily-enterprises`. This preview selects the entire
`vibe64-getting-started` topic at release `0.2.0`, grouped under the `vibe64`
domain. It is the first Learning v2 release: every lesson uses lesson format v2,
a list of short steps the learner reads in the Learning environment (**L**)
without needing AI. **Teach me** asks Colleague to explain the current step on
the real screens and **Show me** points at the place a step talks about.
Colleague never grades: a step passes only through an automatic check, a choice
question compared on the server, or the learner's own **Done**. Each lesson has
learner-facing **Lesson notes**.

| Code | Lesson |
| --- | --- |
| V64-START-00 | Connect your AI (no practice project) |
| V64-START-01 | Your first steps in Vibe64 (Preview press checked automatically) |
| V64-START-02 | Make your first change (code check on `greeting.mjs`; requires 01) |
| V64-START-03 | Build with a database (SQLite notes app; requires 01) |

Lessons 1–3 each create a practice project, an ordinary project marked as
practice that the learner can delete with one click.

The 0.2.0 manifest and generated lock pin topic commit
`07e482d07c74d89ed3373894fe1082a7f17722ea` (manifest hash
`7632617db521c96724760735157f82af5eeb0db4cdfb8c6a8d8275ef57988846`). Every
lesson has new content and a new hash, so passes from 0.1.x lessons are not
credited against them. Earlier releases stay listed in `topics.json` with their
retained commits (0.1.11 at `0c0865c63ce81d7ce501be55d221c2ccda7244b6`), and
installed learner pins remain intact: v1 attempts stay readable but cannot be
continued. Installing 0.2.0 from Learning → Courses (**Install**, or **Update**
from 0.1.11) enables it and disables older enabled releases of the same course
for new starts only. 0.2.0 needs a Vibe64 version with Learning v2; publish this
catalogue on `main` only after that version is deployed. Because it is a
preview, only the workspace owner can start its lessons, with **Try preview**;
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
