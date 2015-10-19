## Install

```
mkdir ~/.dotfiles
git clone git@github.com:mshauneu/dotfiles.git ~/.dotfiles
git -C ~/.dotfiles submodule update --init --recursive
ln -s ~/.dotfiles/vim/vimrc ~/.vimrc
ln -s ~/.dotfiles/zsh/zshrc ~/.zshrc
ln -s ~/.dotfiles/tmux/tmux.conf ~/.tmux.conf

```
