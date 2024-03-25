# Decision to Implement Pre-commit Hooks

<p style="font-size: 16px;">Date: `2024-03-20`<p>

## Status

Implemented

## Context

Recently, I have identified several areas where I can improve my software development process.
One key element I want to introduce is pre-commit hooks.
Pre-commit hooks are automated scripts executed before committing changes to the repository.
They aim to ensure code consistency, quality, and security.

## Decision

<h3>1. pre-commit-hooks (v3.2.0)</h3>
Repository: https://github.com/pre-commit/pre-commit-hooks<br>
Hooks: <br>
<ul>
<li>trailing-whitespace</li>
<li>end-of-file-fixer</li>
<li>check-yaml</li>
<li>check-added-large-files</li>
<li>requirements-txt-fixer</li>
</ul>

Explanation:
- trailing-whitespace and end-of-file-fixer will help maintain code cleanliness by removing unnecessary white spaces at the end of lines and files.
- check-yaml is essential for our projects utilizing YAML, ensuring syntax correctness.
- check-added-large-files helps avoid committing large files, which can lead to excessive repository size.
- requirements-txt-fixer automates the process of sorting and formatting the requirements.txt file, enhancing readability and dependency management.


<h3>2. black (v23.3.0)</h3>
Repository: https://github.com/psf/black<br>
Hooks: <br>
<ul>
<li>black</li>
</ul>
Explanation: <br>
<ul>
<li>black is a tool for automatic Python code formatting, maintaining a consistent coding style across our projects.</li>
</ul>


<h3>3. bandit (v1.7.5)</h3>
Repository: https://github.com/PyCQA/bandit
Hooks: <br>
<ul>
<li>bandit</li>
</ul>
Explanation: <br>
<ul>
<li>bandit is a tool for static code analysis to identify potential security vulnerabilities. Implementing it will help us identify potential security threats in our codebase.</li>
</ul>

<h3>4. isort (v5.12.0)</h3>
Repository: https://github.com/pycqa/isort
Hooks: <br>
<ul>
<li>isort (python)</li>
</ul>
Explanation: <br>
<ul>
<li>djLint with the djlint-reformat-handlebars hook ensures formatting HTML files according to established standards, contributing to code consistency and readability in our Django projects</li>
</ul>

<h3>5. djLint (v1.34.0)</h3>
Repository: https://github.com/Riverside-Healthcare/djLint
Hooks: <br>
<ul>
<li>djlint-reformat-handlebars (for HTML files)</li>
</ul>
Explanation: <br>
<ul>
<li>djLint with the djlint-reformat-handlebars hook ensures formatting HTML files according to established standards, contributing to code consistency and readability in our Django projects.</li>
</ul>

## Consequences

Implementing the above pre-commit hooks will contribute to:
- Increased code consistency through automated formatting and fixing of stylistic errors.
- Improved code readability by sorting imports and removing unnecessary white spaces.
- Enhanced security by analyzing code for potential threats.
- Streamlined development process through automation of routine tasks.


## Keywords

- Pre-commit
- Hooks