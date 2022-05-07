## My MacOs config...

### Important stuff:
- homebrew
- lazygit
- neofetch
- nvim
- ranger
- zsh

---
#### lazygit
- Install: `brew install lazygit`
Some dependences
- `git-delta` : `brew intall git-delta`

#### nvim
- Install: `brew install nvim`
Some dependences
- Install `pip`, and do `pip install --user pynvim`
- Install `pip3`, and do `pip3 install --user pynvim`
- Install `node`, and do `npm install -g neovim`
- Install `yarn`
- Install `figlet` for inputing text ASCII art

#### ranger
- image preview with *iterm2* `brew insatll iterm2`
- image preview with *kitty* 
	-	`export TERM = xterm-kitty` 
	- `pip3 install pillow ranger-fm`
	- convert command in ImageMagick `brew install imagemagick`
- pdf preview with *pdftoppm* `brew install poppler`

#### kitty
- Install: `brew install kitty`
- Icon: [kitty-icons](https://github.com/DinkDonk/kitty-icon)

#### zathura
- Link: [homebrew-zathura](https://github.com/zegervdv/homebrew-zathura)

##### Installation steps
``` zsh
# install zathura
brew tap zegervdv/zathura
brew install zathura

# install poppler plug
$$ brew install zathura-pdf-poppler
mkdir -p $(brew --prefix zathura)/lib/zathura
ln -s $(brew --prefix zathura-pdf-poppler)/libpdf-poppler.dylib $(brew --prefix zathura)/lib/zathura/libpdf-poppler.dylib brew install zathura-pdf-poppler
mkdir -p $(brew --prefix zathura)/lib/zathura
ln -s $(brew --prefix zathura-pdf-poppler)/libpdf-poppler.dylib $(brew --prefix zathura)/lib/zathura/libpdf-poppler.dylib

# install mupdf plug
brew install zathura-pdf-mupdf
mkdir -p $(brew --prefix zathura)/lib/zathura
ln -s $(brew --prefix zathura-pdf-mupdf)/libpdf-mupdf.dylib $(brew --prefix zathura)/lib/zathura/libpdf-mupdf.dylib
```

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


