---
title: "Post: Conventional Commits"
categories:
  - Blog
tags:
  - conventional
  - specification
---

__Conventional Commit Messages__

See how a minor change to your commit message style can make a difference. [Examples](#examples)

## Commit Formats

### Default

<pre>
<b><a href="#types">&lt;type&gt;</a></b>(<b><a href="#scopes">&lt;optional scope&gt;</a></b>): <b><a href="#subject">&lt;subject&gt;</a></b>
<sub>empty separator line</sub>
<b><a href="#body">&lt;optional body&gt;</a></b>
<sub>empty separator line</sub>
<b><a href="#footer">&lt;optional footer&gt;</a></b>
</pre>

### Merge

<pre>
Merge branch '<b>&lt;branch name&gt;</b>'
</pre>
<sup>Follows default git merge message</sup>

### Types

* API relevant changes
  * `feat` Commits, that adds a new feature
  * `fix` Commits, that fixes a bug
* `refactor` Commits, that rewrite/restructure your code, however does not change any behaviour
  * `perf` Commits are special `refactor` commits, that improve performance
* `style` Commits, that do not affect the meaning (white-space, formatting, missing semi-colons, etc)
* `test` Commits, that add missing tests or correcting existing tests
* `docs` Commits, that affect documentation only
* `build` Commits, that affect build components like build tool, ci pipeline, dependencies, project version, ...
* `ops` Commits, that affect operational components like infrastructure, deployment, backup, recovery, ...
  * `ci` The commit makes changes to continuous integration or continuous delivery scripts or configuration files
* `chore` Miscellaneous commits e.g. modifying `.gitignore`
* `change` The commit changes the implementation of an existing feature
* `security` The commit improves the security of the product or resolves a security issue that has been reported
* `revert` Commits, that revert a previous commit
* `deprecate` The commit deprecates existing functionality, but does not remove it from the product
* `WIP` Commits, that are work in progress

### Scopes

The `scope` provides additional contextual information.

* Is an __optional__ part of the format
* Allowed Scopes depends on the specific project
* Don't use issue identifiers as scopes

### Subject

The `subject` contains a succinct description of the change.

* Is a __mandatory__ part of the format
* Use the imperative, present tense: "change" not "changed" nor "changes"
* Don't capitalize the first letter
* No dot (.) at the end

### Body

The `body` should include the motivation for the change and contrast this with previous behavior.

* Is an __optional__ part of the format
* Use the imperative, present tense: "change" not "changed" nor "changes"
* This is the place to mention issue identifiers and their relations

### Footer

The `footer` should contain any information about __Breaking Changes__ and is also the place to __reference Issues__ that this commit refers to.

* Is an __optional__ part of the format
* __optionally__ reference an issue by its id.
* __Breaking Changes__ should start with the word `BREAKING CHANGES:` followed by space or two newlines. Optionally they may be emphasised by appending a `!` after the type and scope.

Footers are written using the format:

```
<token>: <value>
```

### Examples

```
 feat(shopping cart): add the amazing button
```

```
feat!: remove ticket list endpoint

Refs: JIRA-1337
BREAKING CHANGES: ticket enpoints no longer supports list all entites.
```

```
fix: add missing parameter to service call

The error occurred because of <reasons>.
```

```
build(release): bump version to 1.0.0
```

```
build: update dependencies
```

```
refactor: implement calculation method as recursion
```

```
style: remove empty line
```

Commit message with multi-paragraph body 
and multiple footers

```
fix: prevent racing of requests

Introduce a request id and a reference to latest request. Dismiss
incoming responses other than from latest request.

Remove timeouts which were used to mitigate the racing issue but are
obsolete now.

Reviewed-by: Z
Refs: #123
```

### Notices

> ⚠️ IMPORTANT: The first line of Git commit messages are recommended by some standards to be 52 characters or less to be displayed as titles when body text is present. I try to keep the total length of the <type>, <scope>, and <description> fields to this length if possible.

> ⚠️ IMPORTANT: The maximum length of body lines should not exceed 72 characters. 72 characters is the recommended maximum length to make reading the commit history using the git log command in the terminal. In the terminal, Git will indent commit messages by 8 spaces. Enforcing the 72 character line limit will ensure that the body is readable in the terminal.