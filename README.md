# Epitech Hub Workshop: Tmux

## Introduction

Welcome to the Epitech Hub workshop on Tmux! In this workshop, we will explore the basics of Tmux and learn how to use it effectively for managing terminal sessions.

## Workshop Agenda

1. What is Tmux?
2. Installation and Setup
3. Tmux Basics
   - Creating and managing sessions
   - Splitting panes
   - Navigating between panes
   - Customizing Tmux
4. Conclusion and Resources

## 1. What is Tmux

Tmux is a terminal multiplexer, which means it allows you to manage multiple terminal sessions within a single window. It provides a way to organize and control your terminal environment more efficiently.

With Tmux, you can create and manage multiple sessions, each containing one or more terminal windows or panes. This allows you to work on different tasks or projects simultaneously without needing to open multiple terminal windows or tabs.

## 2. Installation and Setup

Ubuntu / Debian

```sh
apt install tmux
```

Fedora / Centos

```sh
dnf install tmux
```

Archlinux

```sh
pacman -S tmux
```

And you have the config file of Tmux in `.config/tmux` or `.tmux`

## 3. Tmux Basics

### Creating and managing sessions

You can create a new session with this:

```sh
tmux new-session -s SESSION_NAME
```

If you are in tmux you can do it with

```tmux
$PREFIX + :
new -s SESSION_NAME
```

### Splitting panes

Split horizontale

```tmux
$PREFIX + %
```

Split vertical

```tmux
$PREFIX + "
```

### Navigating between panes

To navigate you can do `$PREFIX` with the arrow or the vim keybind

### Customizing Tmux

There is my tmux config

```sh
# Start windows and panes at 1, not 0
set -g base-index 1
set -g pane-base-index 1
set-window-option -g pane-base-index 1
set-option -g renumber-windows on

# activate mouse
set -g mouse on

# change prefix to space
unbind C-b
set -g prefix C-Space
bind C-Space send-prefix
```

You can also install some plugin for tmux with [TPM](https://github.com/tmux-plugins/tpm)

I have this plugin installed

- tmux-plugins/tmux-sensible
- christoomey/vim-tmux-navigator
- dreamsofcode-io/catppuccin-tmux
- tmux-plugins/tmux-yank
- joshmedeski/t-smart-tmux-session-manager

## 4. Conclusion and Resources

- [Tmux official documentation](https://github.com/tmux/tmux/wiki)
- [Tmux Cheat Sheet](https://tmuxcheatsheet.com/)
- [Epitech Hub](https://github.com/Epitech)

Happy Tmuxing!
