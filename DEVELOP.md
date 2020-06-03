# This is the 'develop' branch

The 'develop' branch integrates all open changes which have not yet been accepted into upstream. This is to make sure all work under consideration works together nicely, and works with upstream.

## Other branches

The 'master' branch tracks upstream directly.

New work is always done in a working branch ('pull-' or 'topic-').

A 'carrying' branch will be created if there are PRs rejected from upstream that I still want to carry in my version of the product.

A 'release' branch will be created if I ever intend to stand up this work independently of upstream. This will take selected drops of master plus 'carrying', plus open working branchs I want in the release.

## Merge flow

* working branches merge into develop
* working branches are PR'd into upstream
* working branches rebase on top of master
* upstream merges often into master, develop, carrying
* upstream merges occasionally into release
* release is the only branch that is ever stood up

## PR flow

New work is always done in a working branch ('pull-' or 'topic-').

When ready to submit the PR:

* upstream is merged into master, develop
* working branch is merged into develop, tested
* working branch is rebased onto master, tested
* optionally, working branch is squashed to a single commit if upstream desires it