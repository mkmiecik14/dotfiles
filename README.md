# dotfiles
My MacOS dotfiles setup

Here are the steps to re-create this on another machine

Step 1: install oh-my-bash
This will allow changes to bash themes

```
cd ~/
bash -c "$(curl -fsSL https://raw.githubusercontent.com/ohmybash/oh-my-bash/master/tools/install.sh)"
```

Step 2: clone gruvbox
This is the theme for vim that I like 

```
cd ~/
git clone https://github.com/morhetz/gruvbox.git ~/.vim/pack/default/start/gruvbox
```

Step 3: clone vim-polyglot
This will enable syntax highlighting in vim for a variety of languages

```
cd ~/
git clone --depth 1 https://github.com/sheerun/vim-polyglot ~/.vim/pack/plugins/start/vim-polyglot
```

Step 4: download dotfiles and replace old dot files with symlinks
This will clone the contents of this repo and set up the new dotfiles

This has not been tested yet:
```
cd ~/
git clone https://github.com/mkmiecik14/dotfiles.git
cp .bashrc dotfiles/backups/.bashrc_backup
cp .vimrc dotfiles/backups/.vimrc_backup
ln -s dotfiles/.bashrc ~/.bashrc
ln -s dotfiles/.vimrc ~/.vimrc
```


