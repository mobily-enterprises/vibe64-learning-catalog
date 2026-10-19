# Vibe64 learning catalogue

The initial owner is `mobily-enterprises`. This preview selects the entire
`vibe64-getting-started` topic at release `0.1.11`, grouped under the `vibe64`
domain: Lesson 0 guides private AI account setup, Lesson 1 is the introduction
with chat quizzes, real learner actions and an AI-controlled SVG presentation,
and new Lesson 2, **Make your first change**, is the first code lesson. In it the
learner edits one function in a disposable greeting exercise through
**Dashboard → Files**, sees the new greeting in Preview and presses **Check my
code**; a pinned code check verifies the behaviour (the greeting uses the press
count) rather than exact words, and two short chat questions follow. Main
teaches; Colleague remains the general supervisor.

The 0.1.11 manifest and generated lock pin Topic commit
`0c0865c63ce81d7ce501be55d221c2ccda7244b6`. Lessons 0 and 1 carry the wording
corrections made on the topic's main branch after 0.1.10 (Lesson 0's
account-status checkpoint, Lesson 1's Colleague return path and observable
Preview rubrics), so both have new content hashes compared with 0.1.10; adding
Lesson 2 changed none of their files. Old passes are not automatically credited
against those changed lesson versions. The earlier 0.1.10 release remains pinned
to `a2ac6fa5bdc44cfe604c2f57a83a2a8c261b43ce`, 0.1.9 to
`3410a4a4547fcdf5d5bc4c618b4732018f21d1aa` and 0.1.8 to
`f249bbac26120345c22865b98257b8f22fcfc09e` in their retained Git revisions and
installed snapshots. Earlier registry releases and installed learner pins remain
intact. Preparing this manifest does not install, enable or remotely publish it.
Installing 0.1.11 from Learning's **Courses** pane enables it and disables older
enabled releases of the same course for new starts only; saved attempts keep
their pins. All three lessons are marked published and required. Install it
from Learning → Courses with **Install** (or **Update** from 0.1.10). Because it
is a preview, only the workspace owner can start its lessons, with **Try
preview**; members see it but can start it only once a released course is
published. Native teaching and real learner acceptance remain open.

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
Review learner outcomes and complete all three lessons with real learners before release.
