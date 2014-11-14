dev-notes
=========

## Windows host

### Git
* Use Linux-style line endings: `git config --global core.autocrlf false` before cloning any repos

### Putty
* Settings > Terminal > Features > Tick `Disable application cursor keys mode` - stops it capturing key combinations like `Ctrl <-` and `Ctrl ->`
* Settings > Connection > SSH > Auth > Tick `Allow agent forwarding`
* Settings > Connection > SSH > Auth > Add `Private key for authentication`
* Start `pageant` (ships with Putty) and add SSH key to it - it will then allow forwarding to remote hosts

### tmux
* Putty sends mangled Ctrl modifiers. tmux can ignore them with the following set in .tmux.conf: `set -g terminal-overrides "xterm*:kLFT5=\eOD:kRIT5=\eOC:kUP5=\eOA:kDN5=\eOB:smkx@:rmkx@"`
