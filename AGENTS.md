# AGENTS.md — Doom Emacs Configuration

## Project Overview
Literate Doom Emacs configuration optimized for CS coursework, Org-Roam note-taking, and LaTeX academic writing. Written in Org-mode literate programming format.

## Setup Commands
```bash
# Clone to Doom config directory
git clone https://github.com/boluwajioadepojuworkp/doom-config ~/.doom.d
# Sync and update Doom
doom sync && doom upgrade
```

## Key Modules
- `:lang org +roam2` — Note-taking with Zettelkasten workflow
- `:lang latex +cdlatex +latexmk +lsp` — Academic document preparation
- `:lang python` — Programming and data science
- `:tools lsp` — Language server protocol

## Key Bindings (Org-Roam)
- `<leader> r f` — Find node by modification time
- `<leader> r i` — Insert node link
- `<leader> r b` — Toggle roam buffer (backlinks)

## LaTeX Setup
- AUCTeX for document editing
- CDLaTeX for fast symbol insertion
- LatexMk for automated compilation
- Xenops for live math rendering
- TexLab LSP for autocompletion and diagnostics

## Code Style
- Literate config in `config.org` (not `config.el`)
- Module flags in `init.el` doom block
- Custom snippets in `snippets/` directory
- Screenshots in `images/` for documentation

## Testing
- `doom doctor` — Check for configuration issues
- Verify Org-Roam database syncs: `M-x org-roam-db-sync`
- Test LaTeX compilation with sample document
