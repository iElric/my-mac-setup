# my-mac-setup
Set up my mac dev environment

## Homebrew
`/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
This will also install the XCode command line tools

## Install Iterm2 and oy-my-zsh

### Install 
`brew cask install iterm2`
`brew install wget`
`sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"`

### Customize themes and plugins
* plugins (recommend autojump, dirhisory, git-extras, add to .zshrc):\
https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins#battery

* themes (put downloaded themes under ~/.oh-my-zsh/themes/, change theme in .zshrc):
https://github.com/ohmyzsh/ohmyzsh/wiki/External-themes\
A lot of these themes based on [power fonts](https://github.com/powerline/fonts)


## Install VScode
`brew cask install visual-studio-code`


