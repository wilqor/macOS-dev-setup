# macOS development setup tutorial

## Install Homebrew
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

## Install Cask
```
brew tap caskroom/cask
```

## Install iTerm2
```
brew cask install iterm2
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
sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
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
iTerm2 -> Preferences -> Profiles -> Text -> Change Font
```
There select font `14pt Meslo LG M DZ Regular for Powerline`

## Install ZSH syntax highlighting
```
brew install zsh-syntax-highlighting
```
Open `~/.zshrc` file and write the line below at its end:
```
source /usr/local/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
```

## Install ZSH autosuggestions
```
git clone git://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
```
Edit `~/.zshrc` by setting `plugins=(zsh-autosuggestions)`

Make autosuggestion more visible by writing the line below at the end of `~./zshrc`:
```
ZSH_AUTOSUGGEST_HIGHLIGHT_STYLE='fg=white'
```

Reload ZSH configuration
`source ~/.zshrc`

## Enable ZSH plugins
To activate some of built-in plugins described on [Oh My Zsh page](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins) add 
them in `~/.zshrc` file:
```
plugins=(
  git
  zsh-autosuggestions
  osx
  colored-man
  colorize
)
```

To apply changes reload ZSH configuration
`source ~/.zshrc`

## Enable word jumps in iTerm2
To jump and delete by word - with option key - select `Natural Text Editing` value
from dropdown in:
```
iTerm2 -> Preferences -> Profiles -> Keys -> Load Preset...
``` 

## References
<https://gist.github.com/kevin-smets/8568070>

<http://iampankaj.com/2017/08/27/Awesome-Terminal-Setup-with-iTerm2-ZSH-and-Oh-My-Zsh.html>

<http://sourabhbajaj.com/mac-setup/>