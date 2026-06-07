# dotfiles

My macOS dotfiles, managed with [chezmoi](https://www.chezmoi.io/).

## Bootstrap a new machine

### 1. Install Homebrew

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### 2. Install oh-my-bash

The `.bashrc` uses oh-my-bash with the `minimal-gh` theme and the `git` and `bashmarks` plugins. Install it before applying dotfiles since the installer overwrites `~/.bashrc`.

```bash
bash -c "$(curl -fsSL https://raw.githubusercontent.com/ohmybash/oh-my-bash/master/tools/install.sh)"
```

### 3. Install gruvbox (vim color theme)

```bash
git clone https://github.com/morhetz/gruvbox.git ~/.vim/pack/default/start/gruvbox
```

### 4. Install vim-polyglot (optional, syntax highlighting)

```bash
git clone --depth 1 https://github.com/sheerun/vim-polyglot ~/.vim/pack/plugins/start/vim-polyglot
```

### 5. Install chezmoi and apply dotfiles

```bash
brew install chezmoi
chezmoi init --apply mkmiecik14
```

---

## Managed files

| File | Description |
|------|-------------|
| `.bashrc` | Shell config — oh-my-bash, theme, plugins, aliases |
| `.vimrc` | Vim config — gruvbox theme, line numbers, 80-char column |
| `.gitconfig` | Git identity and preferences |
