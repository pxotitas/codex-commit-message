# Codex Commit Message

A lightweight VSCodium / VS Code extension that generates Git commit messages using your locally installed, ChatGPT-authenticated [Codex CLI](https://github.com/openai/codex).

## Features

- Adds a Codex icon to the Source Control title bar.
- Reads staged, unstaged, and untracked changes.
- Uses recent commit subjects as a style reference.
- Generates a complete commit message and inserts it into the native Git SCM input.
- Never creates the commit or changes the Git staging area.
- Runs Codex in read-only sandbox mode.
- Shows the output channel only when an error needs troubleshooting.

## Requirements

- VSCodium or Visual Studio Code.
- The built-in Git extension enabled.
- [Codex CLI](https://github.com/openai/codex) installed and authenticated with ChatGPT.
- A Git repository open in the editor.

## Usage

1. Open a Git repository.
2. Open **Source Control**.
3. Click the Codex icon in the Source Control title bar.
4. If Codex asks to trust the repository, review and approve the request if you trust that project.
5. Review and edit the generated message before committing.

The extension does not commit on your behalf.

## Configuration

| Setting | Default | Description |
| --- | --- | --- |
| `codexCommit.codexPath` | `/home/px/.local/bin/codex` | Path to the Codex CLI executable. |
| `codexCommit.maxDiffCharacters` | `60000` | Maximum change text sent to Codex. |

Set `codexCommit.codexPath` to the location of your Codex executable on your machine.

## Install from source

Clone this repository and copy the folder into your VS Code extensions directory, or package it as a VSIX with `vsce package`.

## License

MIT
