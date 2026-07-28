# Contributing

## How to start a contribution

The team always encourages early communication for all types of contributions. Found a bug or see something that could be improved? Open an issue. Want to address something bigger like overhauling the entire project? Open an issue or start a Discussion on Github. This way, we can give you guidance and avoid your work being wasted on an implementation which does not fit the project's scope and goal.

Alternatively, submit a pull request with one of the following

* A high-level design of the feature, highlighting goals and key decision points.
* A proof-of-concept implementation.
* In case the change is trivial, you can start with a draft or even provide a PR with the final implementation.

### How we deal with larger features

Implementing a larger feature is usually a very long and
detailed effort. This type of work does not fit well into a single pull request; after several
comment threads it becomes almost unmanageable (for you) and very hard to review (for us). For that
reason, we request the following:

- Submit a design document that supplements the code.
- Submit small pull requests, with each one implementing a single piece of the overall feature.
  Experimental features do not need to work end to end, though these should provide warnings/errors
  for missing functionality when possible.

If, for some reason, you feel this proposed workflow does not fit the feature you're contributing, please reach out to the maintainers so we can provide an alternative.

### Pull request guidelines

Observe the following guidelines when submitting a pull request for review

**Do:**

* Write clear and informative *commit messages*, explain the "WHY"
* Use PR description to provide further explanation or context about the PR topic
* Sign off all your commits ([DCO](https://developercertificate.org))
* Use your full name and a valid, deliverable email address for commit
  authorship. The notion of a "known identity" is open to interpretation. We simply require a real full name
  rather than a pseudonym or handle (sorry, no anonymous contributions). The same applies to your DCO sign-off. If you set
  your `user.name` and `user.email` git configuration options, you can sign your commits
  automatically with `git commit -s`
* Split changes into several self-contained commits
* Rebase frequently
* Amend existing commits rather than add fixup commits during review
* Run linters & unit tests before opening a PR
* Ensure every single commit passes CI

**Don't:**

* Use gitmojis anywhere, they only add noise
* Squash all changes into a single massive commit unless it is a simple or self-contained change

**Tips:**

* Use GitHub comments to further clarify background for the implementation if needed
* Use diagrams, sample code, and links to specific parts of external documentation
* Respond to review comments - responding with "Done" is often enough to indicate that a thread can be resolved
* Resolve trivial (e.g. nitpicks) review threads yourself, leave the rest to the reviewers

### Error message guidelines

We try to keep error messages friendly and actionable.

* If there is a known solution, the error message should politely suggest the solution
  * Include a link to the documentation when suitable
* If there is no known solution, suggest where to look for help
* If retrying is a possible solution, suggest retrying and where to look for help if the issue persists

### Comment guidelines

In general, consider adding comments to the code whenever there exists any context which is not obvious from the code alone. When writing a comment do not repeat how a piece of code works, do explain why this is needed.

If your code was inspired by any third-party sources, consider adding a comment with a link to these sources.

### Test guidelines

When extending an existing feature, please add a new test case instead of modifying any existing ones. Large test scenarios with many branching paths are very hard to understand and to maintain. It is ok to copy and paste large parts of an existing test if needed for a new scenario. It is also fine to add a new parameter group to an existing test, as long as the test function remains unchanged.
