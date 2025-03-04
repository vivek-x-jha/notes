# Dotfiles TODO

## Alfred

1. Sync with [Vivek's Preferences](https://www.dropbox.com/scl/fi/w1dv49koke7bz2m8ltk0n/Alfred.alfredpreferences?rlkey=3af9nssetx5398yuvm03qyhkd&dl=0)
1. Ensure copy buffer enabled
1. Test workflows

## Hammerspoon

Move hammerspoon config to ~/.config/

```sh
cd $XDG_CONFIG_HOME
ln -s ../.dotfiles/hammerspoon
defaults write org.hammerspoon.Hammerspoon MJConfigFile "$XDG_CONFIG_HOME/hammerspoon/init.lua"
rm -rf ~/.hammerspoon
```

## Ble.sh

- Quick install

```sh
git clone --recursive --depth 1 --shallow-submodules https://github.com/akinomyoga/ble.sh.git
make -C ble.sh install PREFIX="$HOME/.local"
rm -rf ble.sh
```

## Zoxide

- demonstrate "jumping" with `j`

- demonstrate "jumping-interactive" with `ji`

## Brew casks

reinstall apps as casks

```sh
brew reinstall --cask --force 1password 1password-cli alfred alt-tab discord figma font-jetbrains-mono-nerd-font google-chrome hammerspoon iterm2 karabiner-elements keycastr postman skim spotify visual-studio-code vlc wezterm whatsapp zoom
```

## Tmux

### Hierarchy

`Session` -> `Window` -> `Pane`

Demonstrate basic aliases: `t`, `ta`, `tl`, `tks`, `tn`

### Core Plugins:

1. Plugin manager: `tpm` (Ensure install works)
1. Move between tmux panes and neovim buffers: `vim-tmux-navigator`
1. Open links: `tmux-fzf-url`
1. Additional keybindings: `tmux-sensible`
1. Copy: `tmux-yank`

### Workspace plugins

1. Session manager: `tmux-fzf`
1. Workspace manager: `tmux-ressurect` + `tmux-continuum`

### Statusline plugins:

1. tmux-mode-indicator
1. tmux-battery
1. tmux-cpu

Commands Cheatsheet:

```sh
tmux list-keys | grep prefix
tmux list-keys | grep copy-mode
```
