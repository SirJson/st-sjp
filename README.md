# st-sjp

[st is a simple terminal emulator for X](https://st.suckless.org/) which sucks less.

This is a version of latest master branch @ https://git.suckless.org/st as of today (commit: 51e19ea11dd42eefed1ca136ee3f6be975f618b1) with patches applied that I found useful. 

_(+ some very minor tweaks, patching can get messy and I use st together with Powerlevel10k so it is preconfigured for that)_

Since this is based on a not yet released version of st with a bunch of diffs on top this is more or less unsupported.
What you see here exists so that I don't have to redo the same work over and over again. Maybe it can help you save the time if you agree with my patch selection.

## Pre-applied patches

- Scrollback (Keyboard only!)
- External pipe patch + SIGUSR1 patch
- New terminal in current directory
- Bold is not bright
- Dracula (Because I _really_ like this theme)

I also included all source diffs in the folder "patches" and made a commit for every applied patch. So it should be possible to go back and have a leaner version if you want.

## Requirements

In order to build st you need the Xlib header files.

## Installation

Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install

## Running st

If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

## Credits

Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.
