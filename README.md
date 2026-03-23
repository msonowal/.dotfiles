# Dotfiles

Managed with [chezmoi](https://chezmoi.io/).

## Fresh Machine Setup

```bash
# 1. Install Homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
eval "$(/opt/homebrew/bin/brew shellenv)"

# 2. Install chezmoi and apply dotfiles (install script runs automatically)
brew install chezmoi
chezmoi init --apply msonowal
```

This will configure: zsh, starship prompt, git, cmux terminal, and install all brew packages/casks.

## Post-Setup (Manual)

- Import GPG keys for git commit signing
- Set up SSH keys for GitHub
- Configure git user per-directory (`.gitconfig.personal` / `.gitconfig.work`)
- Install Laravel Valet: `composer global require laravel/valet && valet install`
- Link PHP for Valet: `valet use php@8.5`

## Managed Files

| File | Purpose |
|------|---------|
| `.zshrc` | Shell config, aliases, plugins |
| `.gitconfig` | Git settings, GPG signing, includeIf per-directory |
| `.config/ghostty/config` | Terminal config (used by cmux) |
| `.config/starship.toml` | Prompt theme |

## Day-to-Day

After editing a managed file locally:

```bash
chezmoi re-add          # update source from local
chezmoi cd              # cd into source dir
git add -A && git commit -m "description" && git push
```
