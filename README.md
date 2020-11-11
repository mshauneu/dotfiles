# DotFiles

My `dotfiles` configuration

## Install

```sh
mkdir ~/.dotfiles
git clone https://github.com/mshauneu/dotfiles.git ~/.dotfiles
git -C ~/.dotfiles submodule update --init --recursive
ln -s ~/.dotfiles/vim ~/.vim
ln -s ~/.dotfiles/vim/vimrc ~/.vimrc
ln -s ~/.dotfiles/zsh/zshrc ~/.zshrc
ln -s ~/.dotfiles/tmux/tmux.conf ~/.tmux.conf
```

## Add

```sh
git submodule add https://github.com/ctrlpvim/ctrlp.vim vim/pack/plugins/start/vim-ctrlp
```

## Remove

```sh
git submodule deinit vim/pack/plugins/start/vim-ctrlp
git rm vim/pack/plugins/start/vim-ctrlp
rm -Rf .git/modules/vim/pack/plugins/start/vim-ctrlp
```

## Remove (Alt)

```sh
git submodule | grep ctrl | awk '{print $2}' | xargs -I % echo "git submodule deinit % ; git rm % ; rm -Rf .git/modules/%" | sh
```
