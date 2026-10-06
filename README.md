# Vibe64 learning catalogue

The initial owner is `mobily-enterprises`. This local preview selects the entire
`vibe64-getting-started` topic at release `0.1.2`: ONE introduction to using
Vibe64, with chat quizzes, real learner actions and an AI-controlled SVG. There
are no further lessons in this sprint. Content is still preview; native teaching
integration and a real learner trial must pass before it is an accepted release.

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
