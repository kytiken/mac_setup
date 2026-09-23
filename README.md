# Mac setup

Homebrew パッケージ・macOS 設定・dotfiles はすべて [kytiken/dotfiles](https://github.com/kytiken/dotfiles)（chezmoi）で管理している。

## install

1. install homebrew

   ```shell
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

1. apply dotfiles

   Brewfile のインストール、macOS の defaults 設定、fisher プラグインのインストールもここで実行される。

   ```shell
   /opt/homebrew/bin/brew install chezmoi
   chezmoi init --apply git@github.com:kytiken/dotfiles.git
   ```

1. change default shell

   ```shell
   sudo sh -c 'which fish >> /etc/shells'
   ```

   ```shell
   chsh -s $(which fish)
   ```

1. import Raycast settings

   `config_files/Raycast.rayconfig` を Raycast の Import Settings & Data から読み込む。

## update

- Homebrew パッケージ: `chezmoi cd` で移動して `Brewfile` を編集し、`chezmoi apply`（Brewfile が変わったときだけ `brew bundle` が走る）
- fish プラグイン: `fisher install ...` 後に `chezmoi re-add ~/.config/fish/fish_plugins`
