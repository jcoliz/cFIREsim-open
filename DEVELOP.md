# This is the 'develop' branch

The 'develop' branch integrates all open changes which have not yet been accepted into upstream. This is to make sure all work under consideration works together nicely, and works with upstream.

## Other branches

The 'master' branch tracks upstream directly.

New work is always done in a working branch ('pull-' or 'topic-').

## Merge flow

* working branches merge into develop
* working branches are PR'd into upstream
* upstream merges into master, develop
* working branches rebase on top of master
* release branch will be created if I ever intend to stand up this work independently of upstream. this will take master plus open working branchs I want in the release

## PR flow

New work is always done in a working branch ('pull-' or 'topic-').

When ready to submit the PR:

* upstream is merged into master, develop
* working branch is merged into develop, tested
* working branch is rebased onto master, tested
* optionally, working branch is squashed to a single commit if upstream desires it