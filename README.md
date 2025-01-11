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
   ansible-playbook -i hosts -K playbook.yml
   ```

1. fish setup

   - install fisher
     - [GitHub - jorgebucaran/fisher: A plugin manager for Fish](https://github.com/jorgebucaran/fisher)

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

### install tpm

```shell
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

```shell
ln -s (pwd)/config_files/tmux.conf.local ~/.tmux.conf.local
```
