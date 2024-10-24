# gh-automerge

A GitHub (`gh`) CLI extension for enabling auto-merge on a pull request.

- Uses the pull request title and number for the merge commit message subject:

	> Create auto-merge extension (#1234)

- Generates a body for the merge commit.
- If the branch contains more than one commit, asks if you want to use a specific commit or all commits (formatted as a markdown list) for the merge commit body.
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
3. Ensure you have `fzf` installed.

## Usage

```shell
# In a GitHub repository

gh automerge
```
