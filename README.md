oh-my-zsh-danlinn-theme
=======================

NEW: rvm ruby version displayed before the battery
charge on the right side

This repo contains a theme called danlinn that combines
the Powerline-like agnoster theme and the multi-line 
duellj theme and includes a battery display script 
(adapted from Steve Losh's) that shows 
charging/plugged-in (not charging) and the charge level.
Includes the mensch-powerline font for fancy symbols.  

Install (this assumes that you have the original 
oh-my-zsh installed):

1. Put the themes/danlinn.zsh-theme file in your oh-my-zsh
themes folder. (Mine is at ~/.oh-my-zsh/themes/)

2. Install the font

3. Symlink or whatever the batterycharge.py to 
bin/batterycharge.py and add execute priviliges to it

4. Switch your terminal font to mensh

5. Play with colors - some colors may need ot be changed for maximum contrast.  I leave that to you.

6. In your ~/.zshrc file add this function:
function ruby_version() {
  if which rvm-prompt &> /dev/null; then
    rvm-prompt i v g
  else
    if which rbenv &> /dev/null; then
      rbenv version | sed -e "s/ (set.*$//"
    fi
  fi
}

7. Then switch your theme to danlinn

Enjoy
