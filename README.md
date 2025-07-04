# Go Template

![License](https://img.shields.io/github/license/FollowTheProcess/go-template.svg)

A clean, simple Go copier template.

## Features

### Choose Project Type

The template lets you choose whether you want to create a binary executable program (e.g. a CLI) or an importable library and the generated files will be tailored accordingly! For example, a binary project will use [goreleaser] and have a `build` target in the task runner to compile it.

> [!NOTE]
> If you choose a binary, by default the `release` GitHub action will use [goreleaser] to create a homebrew cask for your program. This requires you to have a homebrew tap repo under your username like `FollowTheProcess/homebrew-tap` and to set a [repository secret] called `HOMEBREW_TAP_TOKEN` containing a GitHub [personal access token] with permissions to write to that repo

### [GitHub Actions]

The project template comes with a ready to go GitHub Actions configuration file which automates all your code quality checks:

* Testing with `go test`
* Linting with [golangci-lint] or [staticcheck]
* Formatting with `go fmt`
* Dependency updates with [Dependabot] or [Renovate]

### Automation with [Task]

Very clean and simple `Taskfile.yml` to automate project maintenance and development

### GitHub Issue Labelling

Series of helpful labels that you can use to categorise issues and pull requests. These come in especially handy when combined with the Release Drafter workflow!

### Automatic Release Drafts

Automatically generate release notes with the [Release Drafter] workflow. This uses the labels from issues and pull requests to draft pretty and detailed release notes for your GitHub releases.

This is automatically run when you push a new tag to main.

## Usage

* Ensure you have [copier] installed (I'm using [uv] here):

``` shell
uv tool install copier
```

* Call copier with this template and answer all the questions

``` shell
copier copy gh:FollowTheProcess/go-template /path/to/put/your/new/project
```

* Create a git repo and start developing

* Make a first commit to set up the github repo

* That should be it! from now on everything will be handled automatically. All you need to do is write code, tests and docs! Your code will be style checked, your tests will be run etc.

[GitHub actions]: https://docs.github.com/en/free-pro-team@latest/actions
[golangci-lint]: https://golangci-lint.run
[staticcheck]: https://staticcheck.dev
[goreleaser]: https://goreleaser.com/intro/
[copier]: https://github.com/copier-org/copier
[Task]: https://taskfile.dev
[repository secret]: https://docs.github.com/en/actions/security-for-github-actions/security-guides/using-secrets-in-github-actions
[personal access token]: https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens
[Dependabot]: https://github.com/dependabot
[Renovate]: https://www.mend.io/renovate/
[uv]: https://docs.astral.sh/uv/
