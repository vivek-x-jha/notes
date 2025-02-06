# BUG: zsh compinit - insecure directories

- test solution:

```sh
chmod -R go-w "$(brew --prefix)/share/zsh/site-functions"
chmod -R go-w "$(brew --prefix)/share/zsh-completions"
```

# BUG: 1Password ssh agent custom vault

- test solution:

```sh
cat <<EOF > "$XDG_CONFIG_HOME/1Password/ssh/agent.toml"
# https://developer.1password.com/docs/ssh/agent/config

[[ssh-keys]]
item = "GitHub Signing Key"
vault = "Ari's Passwords"
EOF
```

# TODO: Configure touchid for sudo

- Ensure pam-reattach installed

```sh
brew list pam-reattach &>/dev/null || brew install pam-reattach
```

- change from /opt/homebrew/ to /usr/local and check path is valid for: /usr/local/lib/pam/pam_reattach.so

```sh
bat /etc/pam.d/sudo_local
sudo cp -f ~/.dotfiles/sudo/sudo_local /etc/pam.d/sudo_local
bat /etc/pam.d/sudo_local
```

# TODO: Migrate app management to homebrew

- Delete manually downloaded versions from `/Applications/` - some app downloads may require sudo authentication

```sh
brew install --cask 1password alfred alt-tab chatgpt discord font-jetbrains-mono-nerd-font google-chrome hammerspoon iterm2 karabiner-elements postman skim spotify visual-studio-code vlc wezterm zoom
```
