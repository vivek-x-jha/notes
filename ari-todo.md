# Dotfiles TODO

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
