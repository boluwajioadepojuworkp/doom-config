# AGENTS.md — Doom Emacs Configuration

## Repository Layout
- `init.el` — Doom Emacs entry point. Declares modules and flags.
- `config.org` — Literate configuration in Org-mode format. All customization lives here.
- `snippets/` — YASnippet templates for code generation.
- `images/` — Screenshots for documentation.

## Building and Testing
```bash
# Clone to Doom config directory
git clone https://github.com/boluwajioadepojuworkp/doom-config ~/.doom.d

# Sync packages and apply configuration
doom sync && doom upgrade

# Run health checks
doom doctor
```

## Key Modules
| Module | Flags | Purpose |
|--------|-------|---------|
| `:lang org` | `+roam2` | Note-taking with Zettelkasten workflow, Org-Roam database |
| `:lang latex` | `+cdlatex +latexmk +lsp` | Academic writing with live preview and code intelligence |
| `:lang python` | — | Programming, data science, literate programming |
| `:tools lsp` | — | Language server protocol for autocompletion and diagnostics |

## Key Bindings
- `<leader> r f` — Find Org-Roam node by modification time
- `<leader> r i` — Insert Org-Roam link with automatic lowercase
- `<leader> r b` — Toggle roam buffer (backlinks)
- `<leader> r t` — Add tag to node

## General Guidance
- Configuration is literate: edit `config.org`, not raw Elisp files.
- Org-Roam notes directory: `~/Notes`.
- LaTeX compilation uses LatexMk for automatic dependency resolution.
- Math rendering uses Xenops for asynchronous SVG preview.
- Code intelligence uses TexLab LSP server.

## Commit Messages
- Follow the [Chris Beams](http://chris.beams.io/posts/git-commit-style/) style.
- Every commit should answer: what changed and why.

## Review Checklist
- `doom doctor` reports no errors.
- Org-Roam database syncs without errors.
- LaTeX compilation succeeds on a test document.
- No broken image references in `config.org`.
