# Setting Up Node and NVM
*Estimated time to complete: ~30 mins*

### Background
> In order to effectively develop for the web, you need to be able to run Javascript on your computer. The most effective way to do this is to us Node.js, which is more or less a wrapper around V8 (the javascript engine in Chrome).

### Plan of action
We will be installing Node using Node Version Manager(NVM). This will allow us to change node versions easily between multiple projects, as well as allow us to easily install new node versions and updates.


## Installing NVM and then Node (Mac)

Prerequisites: Your computer should have homebrew installed. If not refer to the Homebrew installations page.

#### Make sure you are in the home directory
Simply type: `cd` to get there

#### Clear out old version of Node along with their dependencies

```
brew uninstall --ignore-dependencies node
brew uninstall --force node
```

#### Update your current install of Homebrew
This just serves to make sure things are up to date and working

```
brew update
```

#### Install NVM

```
brew install nvm
```

#### Making a directory for NVM to use
NVM will need a place to manage versions, dependency, and other config things. This folder may or may not exist

```
mkdir ~/.nvm
```

#### Adding NVM to path
**For MacOS Catalina and later editions of MacOS, Apple switch the default terminal to zsh.**

For Zsh:
```
echo 'export NVM_DIR="$HOME/.nvm"
[ -s "/usr/local/opt/nvm/nvm.sh" ] && \. "/usr/local/opt/nvm/nvm.sh"
[ -s "/usr/local/opt/nvm/etc/bash_completion" ] && \. "/usr/local/opt/nvm/etc/bash_completion"' >> ~/.zshrc
```
For Bash (Pre Catalina): 
```
echo 'export NVM_DIR="$HOME/.nvm"
[ -s "/usr/local/opt/nvm/nvm.sh" ] && \. "/usr/local/opt/nvm/nvm.sh"
[ -s "/usr/local/opt/nvm/etc/bash_completion" ] && \. "/usr/local/opt/nvm/etc/bash_completion"' >> ~/.bash_profile
```

#### Load the new changes into your terminal

```
source ~/.bash_profile
```

#### Testing of everything worked
You should able to type `nvm ls-remote` and see a list of node versions
If not, please send me a message on slack (Spencer Li) with your error message
and I'll do my best to help you out.

#### Installing Node
Install the latest version of node with the following command

```
nvm install node
```

## Installing NVM and then Node (Windows)
If you already having Node installed without NVM, we'd like you to install it.

You should be able to install NVM with the following command in PowerShell
```winget install -e --id CoreyButler.NVMforWindows```

Then (for some reason) restart your computer to see the changes take effect.

