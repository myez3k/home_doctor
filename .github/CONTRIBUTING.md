
# Contributing to the project

Thank you for your interest in becoming a part of the ongoing development of the project.

This guide covers our practices and recommendations for contributing to the repository.


## Table of Contents

[Ways to contribute](#ways-to-contribute)

[Dev Environment](#dev-environment)

[Pull requests](#pull-requests)

[Commit messages](#commit-messages)


## Ways to contribute

There are various ways to get involved. Here are a few suggestions of things we'd love some help with.

#### Resolving existing issues

 You can consider helping out with issues already requiring attention - look for a "help wanted" label.

#### Reporting issues

If you run into problems in the project, you can report them by opening a new issue and providing as much context as you can about what you're running into, along with a failing test or code sample to help others verify and ultimately fix the issue.

> **Note:** Before filing an issue, please check both open and closed issues to see if the problem has already been reported.

#### Documentation

We are happy to welcome contributions from anyone willing to improve documentation by adding missing information or making it more consistent and coherent.


## Dev Environment

* Install [Node.js](https://nodejs.org/en/), preferably with [nvm](https://github.com/nvm-sh/nvm)

* [Fork the repo and clone your fork](https://docs.github.com/en/get-started/quickstart/fork-a-repo)

* Get all dependencies
  ```
  npm install
  ```
* Add the upstream source for being able to sync main project changes back into your fork. For example, to configure an upstream remote repository for the `eslint-plugin-jsx-a11y` fork, run:
  ```
  git remote add upstream git@github.com:jsx-eslint/eslint-plugin-jsx-a11y.git
  ```
* Run the tests and the build
  ```
  npm test
  ```
* Make and submit changes to the project source files following our [pull request submission workflow](#pull-requests)


## Pull requests

Create a new branch

```
git checkout -b issue1234
```

Commit the changes to your branch, including a coherent commit message that follows our [standards](#commit-messages)

```
git commit -a
```

Before sending the pull request, make sure your code is running on the latest available code by rebasing onto the upstream source

```
git fetch upstream
git rebase upstream/main
```

Verify your changes

```
npm test
# or
npm run tests-only
npm run lint
```

Push your changes

```
git push origin issue1234
```

Send the [pull request](https://docs.github.com/en/pull-requests), make requested changes, and get merged

## Commit messages

* Limit the first line of the commit message (message summary) to 72 characters or less
* Use the present tense and imperative mood when providing a description of what you did
* If your PR addresses an issue, reference it in the body of the commit message
* See the rest of the conventions [here](https://gist.github.com/ljharb/772b0334387a4bee89af24183114b3c7)

#### Commit message example

```
[Tag]: Short description of what you did

Longer description here if necessary

Fixes #1234
```


> **Note:**  Add co-authors to your commit message for commits with multiple authors

```
Co-authored-by: Name Here <email@here>
```
