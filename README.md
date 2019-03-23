# Mac setup

1 install homebrew

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

2 install ansible

```
brew install ansible
```

3 execute playbook

```
ansible-playbook -i hosts -K playbook.yml
```

4 fish setup

```
curl -L https://get.oh-my.fish | fish
omf install rbenv peco nvm
```
