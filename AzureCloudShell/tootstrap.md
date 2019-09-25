#!/usr/bin/pwsh

    mkdir -p ~/Repos/psgivens
    cd ~/Repos/psgivens
    git clone https://github.com/psgivens/computer_setup
    cd computer_setup/AzureCloudShell

    ln -s "$(pwd)/.vimrc" ~/.vimrc
    ln -s "$(pwd)/.tmux.conf" ~/.tmux.conf

### Configure vim for pathogen

    mkdir -p ~/.vim/autoload ~/.vim/bundle && \
    curl -LSso ~/.vim/autoload/pathogen.vim https://tpo.pe/pathogen.vim

### Install vim environment

    git clone https://github.com/ctrlpvim/ctrlp.vim.git ~/.vim/bundle/ctrlp.vim
    git clone https://github.com/jpalardy/vim-slime.git ~/.vim/bundle/vim-slime
    git clone https://github.com/mattn/emmet-vim.git ~/.vim/bundle/emmet-vim
