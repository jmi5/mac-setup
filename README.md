# mac-setup
Steps to set up my Mac


## Intro
I recently went through the process of setting up my Mac at work, I thought I would document the steps and technologies that I installed for easier reference next time. 

**Making keys fast**

* `defaults write -g InitialKeyRepeat -int 10 # normal minimum is 15 (225 ms)`
* `defaults write -g KeyRepeat -int 1 # normal minimum is 2 (30 ms)`

**Homebrew**

Execute `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"` (from https://brew.sh/). 

**fzf**

From https://github.com/junegunn/fzf#installation run:

* `brew install fzf`
* `$(brew --prefix)/opt/fzf/install`

**Copying ssh key**

`pbcopy < ~/.ssh/id_rsa.pub`

**Making `subl`**

Run `sudo ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /usr/local/bin/subl`

**Sublime themes**

I currently have GravityOne installed. 

* Cmd-Shift-P -> "Install Package Manager"
* Then Cmd-Shift-P -> "Package Control: Install Package"
* Cmd-Shift-P -> "UI: Select Theme" AND then "UI: Select Color Theme" so that both sidebar and text change. 

Link to themes: https://dev.to/kazup/10-best-sublime-text-themes-in-2018-53j5

**Syntax highlighting - Sublime**

Protobuf syntax: https://packagecontrol.io/packages/Protocol%20Buffer%20Syntax - Cmd-Shift-P -> "Protocol Buffer Syntax"

**Syntax highlighting - Vim**

`vi ~/.vimrc` and add 

```vim
filetype plugin indent on
:syntax on
```

**Markdown preview in Sublime**

https://facelessuser.github.io/MarkdownPreview/usage/

**My `.zshrc`**

```bash
## Josh's random stuff
alias rvs="cd ~/git/rvstash"
alias protom="rvs && cd protobuf-models"
```







