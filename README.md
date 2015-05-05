git-shell-commands
==================

This repository contains a small set of commands for managing a simple git server that uses
a git user with a git-shell.

Setup the git server
--------------------

These steps were tested on an Ubuntu Server 14.04.2 installation.

```sh
sudo apt-get install git
sudo adduser --system --group --shell /usr/bin/git-shell git

sudo -H -u git -s
cd ~
umask 0007
mkdir ~/.ssh
chmod 700 ~/.ssh
touch .ssh/authorized_keys
chmod 600 .ssh/authorized_keys
git clone https://github.com/henriqueqc/git-shell-commands.git
```

