## My MacOs config...

### Important stuff:
- lazygit
- neofetch
- nvim
- ranger
- zsh

---

#### nvim

Some dependences
- Install `pip`, and do `pip install --user pynvim`
- Install `pip3`, and do `pip3 install --user pynvim`
- Install `node`, and do `npm install -g neovim`
- Install `yarn`
- Install `figlet` for inputing text ASCII art

#### ranger

- image preview with *iterm2* `brew insatll iterm2`
- pdf preview with *pdftoppm* `brew install poppler`

#### zsh

Add environment variables in `/etc/zshrc`
``` bash
export ZDOTDIR="$HOME/.config/zsh"
export ZIM_HOME="$HOME/.config/zim"
```

Initial configuration

``` bash
chsh -s /bin/zsh "$name" >/dev/null 2>&1
sudo -u "$name" mkdir -p "$HOME/.local/share/zsh/"
sudo -u "$name" touch "$HOME/.local/share/zsh/history"
sudo -u "$name" ln $HOME/.config/zsh/init/zshenv $HOME/.config/zsh/.zshenv
sudo -u "$name" cp $HOME/.config/zsh/init/zshrc $HOME/.config/zsh/.zshrc
sudo -u "$name" ln $HOME/.config/zsh/init/zlogin $HOME/.config/zsh/.zlogin
sudo -u "$name" cp $HOME/.config/zsh/init/zimrc $HOME/.config/zsh/.zimrc
sudo -u "$name" mkdir -p "$HOME/.config/zim/"
sudo -u "$name" cp $HOME/.config/zsh/init/zimfw.zsh $HOME/.config/zim
```


