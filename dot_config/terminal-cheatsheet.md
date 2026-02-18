# Terminal Cheat Sheet

## Ghostty

| Shortcut | What it does |
|---|---|
| `Cmd+`` ` | Toggle quick drop-down terminal (from any app) |
| `Cmd+T` | New tab |
| `Cmd+W` | Close tab |
| `Cmd+Shift+[` / `]` | Switch tabs |
| `Cmd+D` | Split right |
| `Cmd+Shift+D` | Split down |
| `Cmd+[` / `]` | Switch splits |

## fzf (Fuzzy Finder)

| Shortcut | What it does |
|---|---|
| `Ctrl+R` | Fuzzy search command history |
| `Ctrl+T` | Fuzzy file finder with bat preview |
| `Alt+C` | Fuzzy cd into directories |

## Modern CLI Aliases

| Command | Runs | What it does |
|---|---|---|
| `cat <file>` | bat | Syntax-highlighted file output |
| `ls` | eza | Icons + grouped directories |
| `ll` | eza -la | Detailed list with icons |
| `lt` | eza --tree | Tree view (2 levels) |
| `top` | htop | Interactive process viewer |
| `diff` | delta | Side-by-side colored diff |
| `git diff` | delta | Side-by-side git diff (auto via gitconfig) |

## Zsh Features

| Feature | How |
|---|---|
| Autosuggestions | Type a previous command, press `→` to accept |
| Syntax highlighting | Invalid commands turn red, valid turn green |
| Smart cd (zoxide) | `z <partial-path>` — learns from your visits |

## Laravel

| Alias | Command |
|---|---|
| `art` | `php artisan` |
| `artm` | `php artisan migrate` |
| `artmf` | `php artisan migrate:fresh --seed` |
| `tinker` | `php artisan tinker` |
| `sail` | `vendor/bin/sail` |

## Chezmoi (Dotfiles)

| Command | What it does |
|---|---|
| `chezmoi diff` | See what changed vs repo |
| `chezmoi apply` | Re-apply configs from repo |
| `chezmoi add <file>` | Track a new config file |
| `chezmoi cd` | cd into dotfiles source repo |
| `chezmoi update` | Pull latest from remote + apply |

### Fresh machine setup
```bash
sh -c "$(curl -fsLS get.chezmoi.io)" -- init --apply msonowal --ssh
```
