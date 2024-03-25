# Dotfiles

## Core Installations

Install the Command Line Tools to help Homebrew to compile things

```
xcode-select --install
```

**Hook up some git configs**

```
git config --global pull.ff only
git config --global alias.st status
```

Get [homebrew](https://brew.sh/) itself so we can run `brew`

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Get both [npm](https://nodejs.org/en/download) and [pnpm](https://pnpm.io/fr/installation#en-utilisant-homebrew)

```
brew install node
brew install pnpm
```

## Create Workspace repository

```
mkdir ~/Workspace
```

## Setting up Hyper.js to get rid of Terminal

### Initial setup

Downloading hyper.js itself

```
brew install --cask hyper visual-studio-code
```

Add the content from `.hyper.js` to your local one and perform a Full Reload *(View > Full Reload)*


### Setting up zsh with autosuggestions and syntax highlighting

```
brew install zsh
chsh -s /bin/zsh // replaces bash with zsh
```

Get [Oh My Zsh](https://ohmyz.sh/)

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
Install `zsh-autosuggestions` and `zsh-syntax-highlighting`

```
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
```

Install [pure](https://github.com/sindresorhus/pure)

```
brew install pure
```

Add the content from `.zshrc` to your local one and perform a Full Reload *(View > Full Reload)*

### Installing [nvm](https://github.com/nvm-sh/nvm#install--update-script)

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```