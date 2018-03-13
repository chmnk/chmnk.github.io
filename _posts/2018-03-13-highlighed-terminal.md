---
layout: post
title: "Highlighted terminal"
date: 2018-03-13
---
For some reasons, the terminals on my Ubuntu computers sometimes loose their nice syntax highligthing. Or I just forget to enable it since it is sometimes disabled by default.
Here is the correct .bashrc :

for prompt either just uncomment this if the prompt highlight settings are already in the .bashrc file 
```bash
force_color_prompt=yes
```
or 
```bash 
color_prompt=yes
PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$ '
fi
``` 
for ls
```bash
if [ -x /usr/bin/dircolors ]; then
    test -r ~/.dircolors && eval "$(dircolors -b ~/.dircolors)" || eval "$(dircolors -b)"
    alias ls='ls --color=auto'
    #alias dir='dir --color=auto'
    #alias vdir='vdir --color=auto'

    alias grep='grep --color=auto'
    alias fgrep='fgrep --color=auto'
    alias egrep='egrep --color=auto'
fi
```
