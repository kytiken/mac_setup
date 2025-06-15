# Mac setup

## install

1. install homebrew

   ```
   /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
   ```

1. install ansible

   ```
   brew install ansible
   ```

1. execute playbook

   ```
   ansible-playbook main.yml
   ```

1. fish setup

   - install fisher
     - [GitHub - jorgebucaran/fisher: A plugin manager for Fish](https://github.com/jorgebucaran/fisher)

1. fix fish path

   ```
   ln -s (pwd)/config_files/0_fish_macos_set_env_path.fish ~/.config/fish/conf.d/0_fish_macos_set_env_path.fish
   ```

1. install fish plugin

   ```
   cat plugins/fish_plugins | fisher install
   ```

1. configure asdf

   ```
   cat plugins/asdf_plugins | xargs -IPLUGIN_NAME asdf plugin add PLUGIN_NAME
   ```

## update plugin files

### fish_plugins

```shell
fisher list > plugins/fish_plugins
```

### asdf_plugins

```shell
asdf plugin list > plugins/asdf_plugins
```

### install oh-my-tmux

```shell
git clone --single-branch https://github.com/gpakosz/.tmux.git ~/.tmux
```

```shell
ln -s $HOME/.tmux/.tmux.conf $HOME/.tmux.conf
```

```shell
ln -s (pwd)/config_files/tmux.conf.local ~/.tmux.conf.local
```
