# macOS development setup tutorial
> This tutorial was tested on macOS Ventura (13.3.1).

## Install Homebrew
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
Follow commands in the end of the installation completed message.
Cask is already included.

## Install iTerm2
```
brew install iterm2
```

## Configure iTerm2
Set theme to `Solarized Dark` by selecting it in:
```
iTerm2 -> Preferences -> Profiles -> Colors -> Colors Presets dropdown
```

Enable unlimited scrollback by checking option in:
```
iTerm2 -> Preferences -> Profiles -> Terminal -> Unlimited scrollback
```

## Install wget
```
brew install wget
```

## Install zsh
```
brew install zsh
```

## Install Oh My Zsh
```
sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```
Edit `~/.zshrc` by setting `ZSH_THEME="agnoster"`.

Reload ZSH
```
source ~/.zshrc
```

## Install Powerfonts
Just follow instructions on <https://github.com/powerline/fonts>

## Configure font
Go to font selection:
```
iTerm2 -> Preferences -> Profiles -> Text -> Font
```
There select font `Meslo LG L DZ for Powerline` and `Regular` and 14 pt.

## Install ZSH syntax highlighting
```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

## Install ZSH autosuggestions
```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```
Make autosuggestion more visible by writing the line below at the end of `~./zshrc`:
```
ZSH_AUTOSUGGEST_HIGHLIGHT_STYLE='fg=white'
```

## Enable ZSH plugins
To activate some of built-in plugins described on [Oh My Zsh page](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins) as well as ZSH syntax highlighting and ZSH autosuggestions add
them in the `plugins` section of the `~/.zshrc` file:
```
plugins=(
  git
  zsh-autosuggestions
  zsh-syntax-highlighting
  macos
  colored-man-pages
  colorize
)
```

To apply changes reload ZSH configuration
`source ~/.zshrc`

## Enable word jumps in iTerm2
To jump and delete by word - with option key - select `Natural Text Editing` value
from dropdown in:
```
iTerm2 -> Preferences -> Profiles -> Keys -> Key Mappings -> Presets...
```
Choose `Keep` option if removing key mappings will will be suggested.

## References
<https://gist.github.com/kevin-smets/8568070>

<http://iampankaj.com/2017/08/27/Awesome-Terminal-Setup-with-iTerm2-ZSH-and-Oh-My-Zsh.html>

<http://sourabhbajaj.com/mac-setup/>
