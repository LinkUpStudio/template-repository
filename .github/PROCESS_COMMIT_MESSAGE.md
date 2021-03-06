# Conventional Commits

## Summary
The Conventional Commits specification is a lightweight convention on top of commit messages. It provides an easy set of rules for creating an explicit commit history. It's easy to describe the features, fixes, and breaking changes made in commit messages.

The commit message should be structured as follows:
```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

The commit contains the following structural elements, to communicate intent to the consumers of your library:

1. **fix**: a commit of the type fix patches a bug in your codebase (this correlates with PATCH in semantic versioning).
1. **feat**: a commit of the type feat introduces a new feature to the codebase (this correlates with MINOR in semantic versioning).
1. **BREAKING CHANGE**: a commit that has a footer BREAKING CHANGE:, or appends a ! after the type/scope, introduces a breaking API change (correlating with MAJOR in semantic versioning). A BREAKING CHANGE can be part of commits of any type.
1. **types** other than fix: and feat: are allowed, we recommend to use build:, ci:, docs:, style:, refactor:, perf:, test:, and others.
1. **footers** other than BREAKING CHANGE: <description> may be provided and follow a convention similar to git trailer format.

## Examples

### Commit message with description and breaking change footer
```
feat: allow provided config object to extend other configs

BREAKING CHANGE: `extends` key in config file is now used for extending other config files
```

### Commit message with `!` to draw attention to breaking change
```
refactor!: drop support for Node 8
```

### Commit message with both ! and BREAKING CHANGE footer
```
refactor!: drop support for Node 8

BREAKING CHANGE: refactor to use JavaScript features not available in Node 8.
```

### Commit message with no body (the most popular type of commit)
```
docs: correct spelling of CHANGELOG
```

### Commit message with scope (use it when you want to describe a part of module or feature)
```
feat(lang): add polish language
```
