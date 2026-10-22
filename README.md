# Vibe64 learning catalogue

The initial owner is `mobily-enterprises`. This preview selects the entire
`vibe64-getting-started` topic at release `0.4.1`, grouped under the `vibe64`
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

The 0.4.1 manifest and generated lock pin topic commit
`20ec27410d9a4c6ffe428393f2d5ea123381b088` (manifest hash
`032206872028cb2274242ecb3a70abb4295fd6ca29974b2dc32414fc44a2c995`). 0.4.1
words Lesson 0 for a learner who has AI: starting it needs the learner's AI,
which prepares its practice project, so its coding chat line no longer assumes
none is connected. 0.4.0
guides every step of **Introduction to Vibe64** with beats that the lesson step
bar plays: it points at each part of the editor, notices when the learner does
what a line asks (sending the change request, reloading Preview, opening a
file, Save, pressing **L**, opening and minimising Colleague) and marks such
steps done. Its first change, **Check it yourself**, is now passed with **Check
my work**: the learner's own AI reviews the practice project's changes against
the step's rubric. Lessons 1–3 are unchanged. 0.3.0
replaced Lesson 0 (Connect your AI) with **Introduction to Vibe64**, a tour of
the editor on a new minimal practice project, and trimmed Lessons 1–3 where
they repeated it; 0.3.1 polishes it after a desktop and phone trial (the tour
app ignores Vibe64's agent guidance directories, so Current changes and Save
show only the learner's change). AI setup is no longer a lesson. Earlier
releases stay listed in `topics.json` with their retained commits (0.4.0 at
`9fe10e8fc8613bacf587f38800b66811cd27a8a9`, 0.3.1 at
`a220f097fa781af49332ff9a44437cfe248a9ac0`, 0.3.0 at
`831af10b660a3b76ac99332caf19c366445ca573`, 0.2.2 at
`996c308abc466b7772985f5576197c7ad1c4178c`, 0.2.1 at
`7fa890a70e2e09faf62d7a3a4ca076304ff63b7f`, 0.2.0 at
`07e482d07c74d89ed3373894fe1082a7f17722ea`, 0.1.11 at
`0c0865c63ce81d7ce501be55d221c2ccda7244b6`), and
installed learner pins remain intact: v1 attempts stay readable but cannot be
continued. Installing 0.4.1 from Learning → Courses (**Install**, or **Update**
from an earlier release) enables it and disables older enabled releases of the same course
for new starts only. 0.4.1 needs a Vibe64 version with Learning v2 and guided
beats with review checks; publish this
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
