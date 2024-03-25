# Decision to Implement Pre-commit Hooks

Date: `2024-03-20`

## Status

Implemented

## Context

Recently, I have identified several areas where I can improve my software development process.
One key element I want to introduce is pre-commit hooks.
Pre-commit hooks are automated scripts executed before committing changes to the repository.
They aim to ensure code consistency, quality, and security.

## Decision

1. pre-commit-hooks (v3.2.0) <br>
Repository: [pre-commit/pre-commit-hooks](https://github.com/pre-commit/pre-commit-hooks) (version v3.2.0) <br>
Hooks:
- trailing-whitespace
- end-of-file-fixer
- check-yaml
- check-added-large-files
- requirements-txt-fixer


## Consequences

Implementing the above pre-commit hooks will contribute to:
- Increased code consistency through automated formatting and fixing of stylistic errors.
- Improved code readability by sorting imports and removing unnecessary white spaces.
- Enhanced security by analyzing code for potential threats.
- Streamlined development process through automation of routine tasks.


## Keywords

- 
- 