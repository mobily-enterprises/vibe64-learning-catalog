# Vibe64 learning catalogue

The initial owner is `mobily-enterprises`. This local preview selects the entire
`vibe64-getting-started` topic at release `0.1.8`: Lesson 0 guides private AI
account setup, followed by ONE introduction with chat quizzes, real learner
actions and AI-controlled SVG presentations. Main teaches; Colleague remains
the general supervisor. The local lock pins reviewed topic commit
`f249bbac26120345c22865b98257b8f22fcfc09e`. Earlier registry releases and installed
learner pins remain intact; this local pin does not install, enable or remotely
publish the candidate. The course remains a local preview. Ordinary Start requires owner installation
and enablement of its exact release, and a lesson marked published; it does not
reject a course merely because the course status is preview. Both selected
lessons are marked published. Isolated author trials use their separate owner
flow. Native teaching and real learner acceptance remain open.

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
Review learner outcomes and complete the single introduction before release.
