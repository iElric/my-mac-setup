# my-mac-setup
Set up my mac dev environment

## Homebrew
`/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`\
This will also install the XCode command line tools

## Install Iterm2 and oy-my-zsh
### Install 
`brew cask install iterm2`\
`brew install wget`\
`sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"`\
iterm has a feature to export and import settings

### Customize themes and plugins
* plugins (recommend autojump, dirhisory, git-extras, add to .zshrc):\
https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins#battery
* themes (put downloaded themes under ~/.oh-my-zsh/themes/, change theme in .zshrc):\
https://github.com/ohmyzsh/ohmyzsh/wiki/External-themes\
A lot of these themes based on [power fonts](https://github.com/powerline/fonts)

## Install VScode
`brew cask install visual-studio-code`\
`settings.json` and `keybindings.json` are at `~/Library/Application Support/Code/User/`\
simply copy from the old machine to the new machine

## Install jenv and jdks
Use [jenv](https://github.com/jenv/jenv) to switch between multiple jdk

### Install
`brew install jenv`

### Set the path in .zshrc
`echo 'export PATH="$HOME/.jenv/bin:$PATH"' >> ~/.zshrc`\
`echo 'eval "$(jenv init -)"' >> ~/.zshrc`\
Use `exec $SHELL -l` to make change effect in current terminal window or simply open a new one\

### Use plugin to set JAVA_HOME
**Do not set JAVA_HOME explicitly**\
`jenv enable-plugin export`\
`exec $SHELL -l`

### Install JDK8
**Oracle no longer provide free JDK, so use openJDK instead**\
See details of [openJDK](https://github.com/AdoptOpenJDK/homebrew-openjdk)\

Add third party repo to brew:\
`brew tap AdoptOpenJDK/openjdk`\
`brew cask install adoptopenjdk8`\

Remove third party repo:\
`brew untap AdoptOpenJDK/openjdk`\

Let the jenv know the jdk location:\
`jenv add $(/usr/libexec/java_home)`\
Or add the absolute jdk path under:
`/Library/Java/JavaVirtualMachines`


## Install pyenv
**TODO**

## Install Hadoop and Spark
**TODO**


