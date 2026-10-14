---
description: Keep README.md up to date when dotfiles are changed
globs:
  - .config/**/*
  - .zshrc
  - .vimrc
  - .tmux.conf
  - .gitignore
  - scripts/**/*
  - LaunchAgents/**/*
  - fzf-git.sh
  - README.md
---

# Dotfiles Documentation Rule

When adding, removing, or reorganizing files tracked in the dotfiles bare repo (`~/.dotfiles/`), update `~/README.md` to reflect the change.

- Add new files/configs to the appropriate section
- Remove entries for deleted files
- Update descriptions if a file's purpose changes
- Keep the table format consistent with existing entries
