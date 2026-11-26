# AGENTS.md

Guidance for coding agents working in this repository.

## Worktrees

Create git worktrees inside `gitignore/`, not anywhere else in the repo:

```bash
git worktree add gitignore/<name> -b <branch>
```

`gitignore/` is ignored by `.gitignore`, so a worktree placed there never shows
up as untracked noise in `git status` and cannot be committed by accident. The
directory itself is kept in the repo by `gitignore/.gitkeep`.

Remove a worktree once its branch is merged or abandoned:

```bash
git worktree remove gitignore/<name>
```
