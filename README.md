# kyanman

KYAN wallet/daemon management utilities - version 0.1.28

* This script installs, updates, and manages single-user kyan daemons and wallets
* It is currently only compatible with 32/64 bit linux.
* Multi-user (system directory) installs are not supported

# Install/Usage

To install kyanman do:

    sudo apt-get install python git unzip pv
    cd ~ && git clone https://github.com/kyancoin/kyanman

To update your existing version 12 32/64bit linux kyan wallet to the latest
kyand, do:

    kyanman/kyanman update

To perform a new install of kyan, do:

    kyanman/kyanman install

To overwrite an existing kyan install, do:

    kyanman/kyanman reinstall

To update kyanman to the latest version, do:

    kyanman/kyanman sync

To restart (or start) kyand, do:

    kyanman/kyanman restart

To get the current status of kyand, do:

    kyanman/kyanman status


# Commands

## sync

"kyanman sync" updates kyanman to the latest version from github

## install

"kyanman install" downloads and initializes a fresh kyan install into ~/.kyancore
unless already present

## reinstall

"kyanman reinstall" downloads and overwrites existing kyan executables, even if
already present

## update

where it all began, "kyanman update" searches for your kyand/kyan-cli
executibles in the current directory, ~/.kyancore, and $PATH.  It will prompt
to install in the first directory found containing both kyand and kyan-cli.
Multiple wallet directories are not supported. The script assumes the host runs
a single instance of kyand.

## restart

"kyanman restart [now]" restarts (or starts) kyand. Searches for kyan-cli/kyand
the current directory, ~/.kyancore, and $PATH. It will prompt to restart if not
given the optional 'now' argument.

<a href="#restart-1">screencap</a>

## status

"kyanman status" interrogates the locally running kyand and displays its status

<a href="#status-1">screencap</a>

# Dependencies

* bash version 4
* nc (netcat)
* curl
* perl
* pv
* python
* unzip
* kyand, kyan-cli - version 12 or greater to update

# Screencaps

### install

<img src="https://raw.githubusercontent.com/moocowmoo/kyanman/master/screencaps/kyanman_0.1-install.png">

### update

<img src="https://raw.githubusercontent.com/moocowmoo/kyanman/master/screencaps/kyanman_0.1-update.png">

### reinstall

<img src="https://raw.githubusercontent.com/moocowmoo/kyanman/master/screencaps/kyanman_0.1-reinstall.png">

### restart

<img src="https://raw.githubusercontent.com/moocowmoo/kyanman/master/screencaps/kyanman_0.1-restart.png">

### status

<img src="https://raw.githubusercontent.com/moocowmoo/kyanman/master/screencaps/kyanman_0.1-status.png">

# Contact

Email me at moocowmoo@masternode.me or submit a pull request.
