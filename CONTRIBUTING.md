# Contributing to Pipeline

Want to go with the flow? Follow the guidelines below to contribute to the project:

#### Table Of Contents

* [Submitting Issues](#submitting-issues)
* [Branching Strategy](#branching-strategy)
* [Pull Requests](#pull-requests)
* [Writing Commit Messages](#writing-commit-messages)

## Submitting Issues

Please check Pipeline's [GitHub issue tracker](https://github.com/new-xkit/pipeline/issues) for known issues.  Additionally, please review the guidelines below before submitting a new issue.

When filing a bug report, please follow the rules below, if applicable:

* Provide information about your environment:
  * Your current versions of your OS, Ruby, Bundler
  * Any other tools you may be using alongside Pipeline
* Provide an easy-to-follow step-by-step process to reliably reproduce the bug
* Include screenshots where possible

## Branching Strategy

* The `production` branch always represents code which is user-facing -- i.e. the most recently deployed production code
* The `master` branch is the central hub for all development work
* Feature branches are branched from `master` when a developer begins work on a feature. Feature branches should have a descriptive name that summarizes the feature on that branch. All work for that feature should be isolated to that branch; it is then submitted as a pull request back to `master` when it is ready for review and merging
* Release candidate branches, formatted as `rc-<MAJOR>.<MINOR>.<PATCH>` (ex. `rc-1.1.0`), are branched from master in preparation for a production deployment; they serve as pre-production snapshots suitable for final bugfixes and release
  * When a release candidate branch receives final approval, it is merged into both `master` and `production` before it is deleted

## Pull Requests

* Use `guard` during development to automatically lint code with [Rubocop](https://github.com/bbatsov/rubocop) and run tests with [RSpec](https://github.com/rspec/rspec)
* Generate [RDoc](http://guides.rubyonrails.org/api_documentation_guidelines.html) documentation as part of your pull request, where applicable
* Include [RSpec tests](https://github.com/rspec/rspec) as part of your pull request, where applicable
* Run `bundle exec rake ci` locally before pushing to ensure a passing build
* [Reference issue numbers](https://help.github.com/articles/closing-issues-via-commit-messages/) in pull request descriptions to automatically close issues resolved by the submission

## Writing Commit Messages

* Use the present tense ("Add feature" not "Added feature")
* Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
* Limit the first line to 50 characters or less
  * This serves as a "subject line" for the commit and should summarize the commit enough to be understandable at a glance
  * Further information should go after a blank line in the commit's "body"
* Wrap subsequent "body" lines at 72 characters
* Focus on explaining _what_ the commit accomplishes and _why_ the change was made instead of the specific mechanics of how it was accomplished, since the "how" can be seen from the code diff

Further reading:

* [5 Useful Tips for a Better Commit Message](https://robots.thoughtbot.com/5-useful-tips-for-a-better-commit-message)
* [A Note About Commit Messages](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
* [How To Write a Git Commit Message](http://chris.beams.io/posts/git-commit/)
