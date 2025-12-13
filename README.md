# Mac setup

## install

1. install homebrew

   ```
   /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
   ```

1. install mise

   ```shell
   curl https://mise.run | sh
   ```

1. install ansible

   ```shell
   mise use pipx@latest
   ```

   ```shell
   mise use ansible
   ```

1. execute playbook

   ```
   ansible-playbook main.yml
   ```

1. change default shell

   ```shell
   sudo sh -c 'which fish >> /etc/shells'
   ```

   ```shell
   chsh -s $(which fish)
   ```

1. ghq get

   ```shell
   ghq get git@github.com:kytiken/mac_setup.git
   ```

   ```
   cd (ghq root)/github.com/kytiken/mac_setup
   ```

1. fish setup

   - install fisher
     - [GitHub - jorgebucaran/fisher: A plugin manager for Fish](https://github.com/jorgebucaran/fisher)

1. install fish plugin

   ```shell
   cat plugins/fish_plugins | fisher install
   ```

1. setting dotfile

   ```shell
   chezmoi init git@github.com:kytiken/dotfiles.git
   ```

   ```shell
   chezmoi apply
   ```

## update plugin files

### fish_plugins

```shell
fisher list > plugins/fish_plugins
```
