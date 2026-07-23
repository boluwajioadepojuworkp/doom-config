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

## Note-Taking System (Org-Roam)
This config implements evidence-based note-taking with spaced repetition,
retrieval practice, and dense concept linking — built on Org-Roam with
Doom Emacs.

### Directory Structure (`~/Notes/`)
| Directory | Purpose | Capture Key |
|-----------|---------|-------------|
| `courses/` | Course index nodes (Week→Lecture→Topics) | `SPC r c c` |
| `lectures/` | Individual lecture notes | `SPC r c l` |
| `topics/` | Atomic topic/concept notes | `SPC r c t` |
| `math/` | Mathematics reference notes (Paul's Notes) | `SPC r c m` |
| `evergreen/` | Permanent/evergreen notes | `SPC r c p` |
| `daily/` | Daily retrieval practice entries | `SPC r c j` |
| `assets/` | Attached files and images | — |
| `images/` | Drag-and-drop images | — |

### Key Bindings
| Key | Action |
|-----|--------|
| `SPC r f` | Find node (by modification time) |
| `SPC r i` | Insert node link (lowercase) |
| `SPC r I` | Insert node link (custom title) |
| `SPC r b` | Toggle roam buffer (backlinks) |
| `SPC r t` | Add tag to node |
| `SPC r T` | Remove tag from node |
| `SPC r v` | Visit node |
| `SPC r u` | Open ORUI graph |
| `SPC r a` | Add alias |
| `SPC r A` | Remove alias |
| `SPC r c` | Capture new note |
| `SPC r j` | Today's daily note |
| `SPC r r` | Random note |
| `SPC r e` | Export to Quartz Markdown |
| `SPC r s` | Search with Deft |

### Note Structure
Two patterns depending on how the course material is organized:

**Week → Lecture → Topics** (for professors who release slides weekly):
```
* Week 1
** Lecture 1
*** Topic 1 → links to topic node
*** Topic 2 → links to topic node
```

**Chapter → Topics** (for professors who follow the textbook):
```
* Chapter 1
** Topic 1 → links to topic node
** Topic 2 → links to topic node
```

### When to Take Notes
1. During lecture: listen actively. Do not transcribe.
2. End of day: write what you remember from memory (retrieval practice).
3. Fill gaps: consult textbook/lecture slides only after attempting recall.

### Export to Quartz
`SPC r e` exports the current org-roam buffer to `~/ME/notes-site/content/`
as Markdown for the Quartz knowledge graph site.

## Key Modules
| Module | Flags | Purpose |
|--------|-------|---------|
| `:lang org` | `+roam2 +dragndrop +gnuplot +pretty` | Note-taking with Zettelkasten, graph visualization, LaTeX |
| `:lang latex` | `+cdlatex +lsp` | Academic writing with live preview and code intelligence |
| `:lang python` | `+lsp +tree-sitter` | Programming, data science |
| `:tools lsp` | `+eglot +booster` | Language server protocol |
| `:tools magit` | — | Git porcelain |
| `:tools pdf` | — | PDF viewing with annotations |

## Commit Messages
- Follow the [Chris Beams](http://chris.beams.io/posts/git-commit-style/) style.
- Every commit should answer: what changed and why.

## Review Checklist
- `doom doctor` reports no errors.
- Org-roam database syncs without errors.
- LaTeX compilation succeeds on a test document.
- Capture templates produce correctly structured notes.
- All keybindings under `SPC r` prefix work as documented.
