# pomod
pomod is a dead-simple Pomodoro timer for Polybar, written in Nim.

![screenshot](screenshot.png)

## Installation
```sh
$ git clone https://github.com/liquid600pgm/pomod.git
$ cd pomod
$ nimble install
$ sudo ln -s $HOME/.nimble/bin/pomod /usr/bin/pomod
```
In your Polybar config:
```ini
[module/pomod]
type = custom/script
exec = pomod
tail = true
format = %{F#f8f8f2}%{u#ff5555}%{+u}<label>%{-u}
click-left = kill -USR1 %pid%
click-middle = kill -USR2 %pid%
```

Nerd Fonts recommended.

## Features

### Pros
 - it's very minimal
 - it's made for use with nerd fonts
 - it has notifications for finished timespans
 - it has a nice, unobtrusive sound

### Cons
 - no configuration unless you edit the source code
 - default config requires nerd fonts
 - the timer's probably imprecise

pomod was mainly made because all the existing online Pomodoro timers suck and
there was no Polybar module for a Pomodoro timer. Well, now there is, and it
doesn't suck (for me at least). Hooray, I guess?

Feel free to use it in your setups, hopefully it can provide itself useful.
