# Zettelkasten Tooling

Mise tasks for managing a zettelkasten with Obsidian. Search, analyze, capture, and maintain your knowledge base from the command line.

## Features

- **Full-text search** across all notes
- **Health dashboard** with stats and broken link detection
- **Quick capture** to inbox without leaving terminal
- **Random note** surfacing for review
- **Graph analysis** for orphans and connections

## Requirements

- macOS or Linux
- [Mise](https://mise.jdx.dev/)
- A zettelkasten following the standard structure

## Installation

Clone this repo and add to your shell config (`~/.zshrc` or `~/.bashrc`):

```shell
git clone https://github.com/ricon-family/zettelkasten.git ~/zettelkasten-tooling
eval "$(mise -C ~/zettelkasten-tooling run -q shell)"
```

Reload your shell, then run `zettel welcome` to verify.

## Quick Start

Create a new zettelkasten:

```shell
zettel init ~/my-zettelkasten
export ZETTEL_ROOT="$HOME/my-zettelkasten"
```

This creates the directory structure, index.md, and CLAUDE.md for AI assistant integration.

## Commands

| Command | Description |
|---------|-------------|
| `zettel init [path]` | Bootstrap a new zettelkasten |
| `zettel welcome` | Overview and current status |
| `zettel search:text <query>` | Full-text search |
| `zettel graph:stats` | Health dashboard |
| `zettel random` | Random note for review |
| `zettel inbox:add <text>` | Quick capture to inbox |

Run `zettel` to see all available commands.

## Structure

This tooling expects a zettelkasten with:

```
zettelkasten/
├── 00_Inbox/          # Raw captures, unprocessed
├── 10_Zettelkasten/   # Permanent atomic notes
└── 99_Archive/        # Source material
```

## See Also

- [shimmer](https://github.com/ricon-family/shimmer) - Agent workflow infrastructure
