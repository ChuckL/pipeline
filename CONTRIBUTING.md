# Contributing to Pipeline

Want to go with the flow? Follow the guidelines below to contribute to the project:

#### Table Of Contents

* [Submitting Issues](#submitting-issues)
* [Branching Strategy](#branching-strategy)
* [Pull Requests](#pull-requests)
* [Git Commit Messages](#git-commit-messages)

## Submitting Issues

* If you want to report an issue, first please read the guidelines below, then submit an issue at https://github.com/new-xkit/pipeline/issues.
* Include screenshots where possible, as well as exact steps to reproduce the bug

## Branching Strategy

* The `production` branch always represents code which is user-facing -- i.e. the most recently deployed production code.
* The `master` branch is the central hub for all development work.
* `feature` branches are branched from `master` when a developer begins work on a feature. All work for that feature should be isolated to that branch; it is then submitted as a pull request back to `master` when it is ready for review and merging.
* `release-candidate` branches (formatted e.g. `rc-1.1.0`) are branched from master in preparation for a production deployment; they serve as pre-production snapshots suitable for final bugfixes and release.
  * When a `release-candidate` branch receives final approval, it is merged into both `master` and `production` and then deleted.

## Pull Requests

* Use `guard` during development to verify your code style against the [Ruby style guide](https://github.com/bbatsov/ruby-style-guide)
* Generate [RDoc](http://guides.rubyonrails.org/api_documentation_guidelines.html) documentation as part of your pull request, where applicable
* Include [RSpec tests](http://rspec.info/) as part of your pull request, where applicable
* Reference issue numbers for closure in PR description when submitting a pull request that resolves an issue
** See https://help.github.com/articles/closing-issues-via-commit-messages/ (these keywords also work in PR descriptions)

## Git Commit Messages

* Use the present tense ("Add feature" not "Added feature")
* Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
* Limit the first line to 72 characters or less
  * This serves as a "subject line" for the commit and should summarize the commit enough to be understandable at a glance.
  * Further information should go after a blank space in the commit's "body".
* Focus on explaining what the commit accomplishes and why the change was made, not the specific mechanics of how it was accomplished (as the "how" can be divined from the code diff).
