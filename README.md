# mac-setup
Steps to set up my Mac


## Intro
I recently went through the process of setting up my Mac at work, I thought I would document the steps and technologies that I installed for easier reference next time. 

Last updated: March 2021.


## Random

**Making keys fast**

* `defaults write -g InitialKeyRepeat -int 10 # normal minimum is 15 (225 ms)`
* `defaults write -g KeyRepeat -int 1 # normal minimum is 2 (30 ms)` 

Then restart the computer, per [this gist](https://gist.github.com/hofmannsven/ff21749b0e6afc50da458bebbd9989c5). 

**Homebrew**

Execute  

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
``` 

(from https://brew.sh). 


**Uninstalling Chrome**

Follow the instructions here: https://chromeisbad.com/#delete. 


**Installing zsh**

Install ZSH from https://ohmyz.sh/. 

```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

You may need to add `export ZSH_DISABLE_COMPFIX=true` to your `~/.zshrc` to disable some warnings. 


**fzf**

From https://github.com/junegunn/fzf#installation run:

* `brew install fzf`
* `$(brew --prefix)/opt/fzf/install`


**Syntax highlighting - Vim**

`vi ~/.vimrc` and add 

```vim
filetype plugin indent on
:syntax on
```

**My `.zshrc`**

```bash
## Josh's random stuff
alias rmlctl="sudo launchctl remove com.opendns.osx.RoamingClientConfigUpdater"
export ZSH_DISABLE_COMPFIX=true
```

## Setting up Github and SSH Keys

Go to https://github.com/settings/keys. Click "add new SSH key". Run `ssh-keygen` in the command line, hit Enter a couple times. Run `pbcopy < ~/.ssh/id_rsa.pub` and paste the result. Navigate to a GH repo and run `ssh -T git@github.com` to check that it worked. 




## Sublime

First, download Sublime Text 3. 

**Making `subl`**

Run `sudo ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /usr/local/bin/subl`. 


**Sublime themes**

I currently have One Dark installed. 

* Cmd-Shift-P -> "Install Package Control"
* Then Cmd-Shift-P -> "Package Control: Install Package"
* Cmd-Shift-P -> "UI: Select Theme" AND then "UI: Select Color Theme" so that both sidebar and text change. 

Link to themes: https://dev.to/kazup/10-best-sublime-text-themes-in-2018-53j5


## Apps I download

* [Spotify](https://www.spotify.com/us/download/other/)
* [Magnet](https://apps.apple.com/us/app/magnet/id441258766?mt=12) for window snapping
* [Tomato One](http://rinik.net/pomodoro/)
* [Whatsapp](https://www.whatsapp.com/download/)
* [Visual Studio Code](https://code.visualstudio.com/download). Type Cmd-Shift-P and install `code` on the PATH. Install Markdown Enhanced Preview as well. 
* Download [R](https://cran.r-project.org/) and [RStudio](https://rstudio.com/products/rstudio/download/#download). 
* [Amphetamine](https://apps.apple.com/us/app/amphetamine/id937984704?mt=12)

**Magnet shortcuts**

`Ctrl-Option-DIRECTION` to move windows. 





