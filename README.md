# Go Copier

![License](https://img.shields.io/github/license/FollowTheProcess/go_copier.svg)

A clean, simple Go project copier template.

## Features

### Choose Project Type

The template lets you choose at creation time whether you want to make an executable binary program, or an importable library. Depending on your choice, the generated files will be tailored to each option!

### [GitHub Actions]

The project template comes with a ready to go GitHub Actions configuration file which automates all your code quality checks:

* Testing with `go test`
* Linting with [golangci-lint]
* Formatting with `go fmt`

### Task Automation with [just]

Very clean, simple justfile to automate project maintenance and development

### [GitHub CLI]

Option to use the new GitHub CLI to create a GitHub repo for you during project creation. (You'll need to have this already installed)

### GitHub Issue Labelling

Series of helpful labels that you can use to categorise issues and pull requests. These come in especially handy when combined with the Release Drafter workflow!

### Automatic Release Drafts

Automatically generate release notes with the [Release Drafter] workflow. This uses the labels from issues and pull requests to draft pretty and detailed release notes for your GitHub releases.

This is automatically run when you push a new tag to main.

## Usage

* Ensure you have [cookiecutter] installed:

``` shell
# pipx
pipx install copier
```

* Navigate to where you keep your projects

* Call cookiecutter with this template and answer all the questions

``` shell
copier gh:FollowTheProcess/go_copier
```

* Create a git repo (if not using the gh cli) and start developing

* Make a first commit to set up the github repo (if you didn't use the gh cli)

* That should be it! from now on everything will be handled automatically. All you need to do is write code, tests and docs! Your code will be style checked, your tests will be run etc.

[GitHub actions]: https://docs.github.com/en/free-pro-team@latest/actions
[GitHub CLI]: https://cli.github.com
[golangci-lint]: https://golangci-lint.run
[FollowTheProcess/go_cli]: https://github.com/FollowTheProcess/go_cli
[just]: https://github.com/casey/just
[cookiecutter]: https://github.com/cookiecutter/cookiecutter