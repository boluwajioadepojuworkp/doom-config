# Doom Emacs Configuration

A literate Emacs configuration built on the Doom Emacs framework, optimized for computer science coursework, academic writing in LaTeX, and networked note-taking with Org-Roam.

## Modules

| Module | Flags | Purpose |
|--------|-------|---------|
| `:lang org` | `+roam2` | Note-taking, knowledge management, Zettelkasten workflow |
| `:lang latex` | `+cdlatex +latexmk +lsp` | Academic document preparation with live preview |
| `:lang python` |: | Programming, data science, literate programming |
| `:tools lsp` |: | Language server protocol for code intelligence |

## Key Bindings

| Prefix | Function |
|--------|----------|
| `<leader> r f` | Find Org-Roam node by modification time |
| `<leader> r i` | Insert Org-Roam link |
| `<leader> r b` | Toggle roam buffer (backlinks) |

## Setup

```bash
git clone https://github.com/boluwajioadepojuworkp/doom-config ~/.doom.d
```

This configuration assumes an existing Doom Emacs installation. See the [Doom Emacs documentation](https://github.com/doomemacs/doomemacs) for installation instructions.

## Note-Taking Workflow

The configuration implements a Zettelkasten workflow adapted for university coursework:
1. Attend lectures without taking notes: focus exclusively on comprehension
2. In the evening, write notes from memory using Org-Roam capture templates
3. Fill gaps using textbooks and lecture materials
4. Link new notes to existing concepts using Org-Roam's node insertion

## License

MIT
