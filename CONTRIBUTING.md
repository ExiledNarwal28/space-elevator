# Contributing to Space Elevator

**Contributions are welcome!**

## Code of conduct

Before contributing to the project, please read our [code of conduct](CODE_OF_CONDUCT.md).

## Task tracking

### Functionnalities to implement

The backlog, functionnaltiies, user stories and use-cases to implement can be found in [this project's wiki](https://github.com/ExiledNarwal28/space-elevator/wiki). You will also find documentation and drafts for planned features.

### Issues

We track our issues with GitHub issues. Each issue must have at least one person assigned, a date of delivery, an associated milestone and correct labels.

Milestones represent release versions. We use [Semanting Versioning 2.0.0](https://semver.org/), which is as follows : `<major>.<minor>.<patch>`.

### Project board

Issues must be placed on the [project board](https://github.com/ExiledNarwal28/space-elevator/projects/1). There are 5 columns in this board : 

- Maybe : Optionnal issues to improve the codebase but with no direct value to the main features
- To do : Issues that must be done to deliver the current iteration
- In progress : Self-explanatory
- Under review : Issues currently in review or waiting to be merged
- Done : Closed issues (see : Definition of done)

The person in charge of an issue is in charge of moving it across the project board.

### Bug reporting

Everything in the app is unit tested. We also have requests and end-to-end tests to run in Postman. It is placed in [/resources](/resources). A test not passing is a bug.

When a bug is spotted in the application, it must be reported as an issue on GitHub issues with the appropriate template. There is a `bug` label. It must be added in the To do column of the project, above all non-bugs issues, ordered by priority.

### Git Flow and pull requests

We use [Git Flow](https://nvie.com/posts/a-successful-git-branching-model/) to separate our branches.

We use trunk based development with `develop` as a main branch. Every PR adding a feature to the application or solving a bug must be merged into `develop`.

For each issue, there must be at least one PR (more PRs could be added if the issue is reopened). This PR must build. Also, two reviewers must approve the PR before it is merged into `develop`. Once it is merged, it will have to pass CI and CD check on `develop`.

PR names are as following : `[CODE] What is added` (ex : `[FEATURE] Add accounts endpoint`).

The one in charge of merging the PR is the one in charge of the associated issue.

To review a PR is a lot of things. First, you must read each added line, understand them, make sur they make sense and point out if there is any way to improve it. You must then pull the branch, test the app, make sure it works in execution using Postman and call it a day. Only approve PRs that are 100% ready to merge. Otherwise, request changes explaining clearly what must be added for approval.

`main` is our production branch. Once in a while, when `develop` is perfectly stable and operationnal, we merge `develop` into `main`.

### Definition of done

A milestone is achieved once every of its issues are solved. This includes everything to add for a new release, from adding features, to solving bugs and improving performance.

Issues are closed once all described tasks are confirmed done by the reviewers, which only means that the PR is closed. This requires reviewing code style, quality, tests and actual functionality of said PR.

## Development

### Code style

We use [Google Java Code Style](https://google.github.io/styleguide/javaguide.html). It is checked pre-commit and during CI check. To format code, use `mvn git-code-format:format-code -Dgcf.globPattern=**/*`.

No comment should be in the source code. Some exceptions are small explanations. In those rare cases, comments are clear and tiny.

TODOs are okay, as long as they do not make it to the release. They can be used to mark where a certain issue must be done (in which case, an issue number is much appreciated). In almost all other cases, they should be removed an converted to an actual issue.

### Test driven development

Every single piece of code added to the application must be written using test driven development. For TDD, we follow the tree basic steps : write failing tests for new feature, write basic code to get tests to pass and finally reformat newly added code. Once the new feature is correctly implemented, commit.

Tests are located in `src/test/java/com/rocknprog/spaceelevator`. The package naming must be identical to `src/main/java/com/rocknprog/spaceelevator`. Test class names must have a `Test` prefix. For instance, the test class for `Main.java` would be `MainTest.java`

Unit tests must have sections Arrange-Act-Assert separated by one blank line. Set up of tests must be extracted as much as possible from unit tests.

## Contributors

- Fabien Roy ([ExiledNarwal28](https://github.com/ExiledNarwal28))
