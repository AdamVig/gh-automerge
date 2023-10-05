# gh-automerge

A GitHub (`gh`) CLI extension for enabling auto-merge on a pull request.

- Uses the pull request title and number for the merge commit message subject:

	> Create auto-merge extension (#1234)

- Generates a body for the merge commit from a commit (defaults to `HEAD`) or from all commits in the branch, formatted as a Markdown list.
- Prompts for confirmation of the merge commit message before proceeding.
- Displays the actual auto-merge commit message after enabling it.
- Adds a warning to the top of the pull request body for reviewers:

	> [!IMPORTANT]
	> **Auto-merge enabled**: approving this pull request will merge it.

## Installation

1. [Install the GitHub CLI](https://github.com/cli/cli#installation).

2. Install the extension.
   ```shell
   gh extension install AdamVig/gh-automerge
   ```

## Usage

```shell
# In a GitHub repository

# To enable auto-merge using HEAD for the body
gh automerge

# Using a specific commit for the body
gh automerge 3bdeb1f30feb17c913b2ca4e0640678e0a69128d

# Using the second-to-last commit for the body
gh automerge HEAD^

# Using all commits in the branch for the body
gh automerge all
```
