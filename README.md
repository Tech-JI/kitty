# Kitty



## Outlook

*The fast, feature-rich, GPU based terminal emulator*

<center class="half">
    <img src="https://s2.loli.net/2024/01/04/ExD4pCyUsg5iGwe.png" width="250"/>
    <img src="https://s2.loli.net/2024/01/04/Pql8YSnL7Maudcm.png" width="500"/>
</center>

This is a set of config files based on [Kitty](https://sw.kovidgoyal.net/kitty/) by [Hydraallen](https://github.com/Hydraallen). 

***

## Introduction

​		*kitty* is designed for power keyboard users. To that end all its controls work with the keyboard (although it fully supports mouse interactions as well). Its configuration is a simple, human editable, single file for easy reproducibility (I like to store configuration in source control).

​		The code in *kitty* is designed to be simple, modular and hackable. It is written in a mix of C (for performance sensitive parts), Python (for easy extensibility and flexibility of the UI) and Go (for the command line [kittens](https://sw.kovidgoyal.net/kitty/glossary/#term-kittens)). It does not depend on any large and complex UI toolkit, using only OpenGL for rendering everything.

​		Finally, *kitty* is designed from the ground up to support all modern terminal features, such as Unicode, true color, bold/italic fonts, text formatting, etc. It even extends existing text formatting escape codes, to add support for features not available elsewhere, such as colored and styled (curly) underlines. One of the design goals of *kitty* is to be easily extensible so that new features can be added in the future with relatively little effort.

***

## Installation

​		Kitty is available in the official repositories of all major Linux distributions, and you can use your favorite package manager to install the *kitty* package. However, note that some Linux distribution packages are woefully outdated. *kitty* is available in a vast number of package repositories for macOS and Linux.

​		To install it, simply open a terminal and type the following command depending on your operating system:

-  On Ubuntu and Debian-based distributions:

```bash
$ sudo apt update && sudo apt install kitty
```

-  On Arch Linux based distributions:

```bash
$ sudo pacman -S kitty
```

- On Fedora Workstation

```bash
$ sudo dnf -y install kitty
```

- On MacOS

```bash
$ brew install kitty
```

​		After the installation process is complete, you can launch it from the Applications menu.

​		By the way, if you’re interested in the original way of installation, you can click [here](https://sw.kovidgoyal.net/kitty/quickstart/) for more information.

***

## Customization

​		Obviously, you can use the default settings and themes in your Kitty terminal, it's very useful. However, I will show you some basic optional customizations that you can apply to your Kitty to make it even more beautiful.

If you don’t want to meet the trouble of configuring your own file, then you can clone sample config file by using:

```bash
git clone git@github.com:Hydraallen/kitty.git ~/.config/kitty/
```

​		Or, if you enjoy these troubleshooting process, then keep to the following steps. 

​		To create a configuration file `~/.config/kitty/` in the directory, you can do it in your manually create a new one in Explorer, or simply tape the following lines into your terminal.:

- For Vim users:

```bash
vim ~/.config/kitty/kitty.conf
```

- For Nano users (not recommanded):

```bash
nano ~/.config/kitty/kitty.conf
```

​		Copy and paste the following lines into the file:

```bash
# font_family      Input Mono 
font_family      Fantasque Sans Mono 
italic_font      auto 
bold_font        auto 
bold_italic_font auto 

# Font size (in pts) 
font_size        18.0 

# The amount the font size is changed by (in pts) when increasing/decreasing 
# the font size in a running terminal. 
font_size_delta 2 

# The foreground color 
foreground       #c0b18b 

# The background color 
background       #202020

# Window Size
remember_window_size yes
shell_integration no-title
```

​		To save the changes and quit, please press `Escape` to exit the vim editor, then type `:wq`. 

​		Nano users can simply press `Ctrl+O` and `Ctrl+X` to save and exit.

<center class="half">
    <img src="https://s2.loli.net/2024/01/04/8gUYjarof2KsReN.png" width="700"/>
</center>
​		Tape `neofetch` if you’ve downloaded. And you may end up with an interface that looks similar to this: 

<center class="half">
    <img src="https://s2.loli.net/2024/01/04/vy3zT5omBOLrCIN.png" width="700"/>
</center>


## Shortcuts

### Tabs

| Action            | Shortcut                                                     |
| ----------------- | ------------------------------------------------------------ |
| New tab           | [`ctrl+shift+t`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.New-tab) (also ⌘+t on macOS) |
| Close tab         | [`ctrl+shift+q`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Close-tab) (also ⌘+w on macOS) |
| Next tab          | [`ctrl+shift+right`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Next-tab) (also ⌃+⇥ and ⇧+⌘+] on macOS) |
| Previous tab      | [`ctrl+shift+left`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Previous-tab) (also ⇧+⌃+⇥ and ⇧+⌘+[ on macOS) |
| Next layout       | [`ctrl+shift+l`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Next-layout) |
| Move tab forward  | [`ctrl+shift+.`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Move-tab-forward) |
| Move tab backward | [`ctrl+shift+,`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Move-tab-backward) |
| Set tab title     | [`ctrl+shift+alt+t`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Set-tab-title) (also ⇧+⌘+i on macOS) |

### Windows

| Action                | Shortcut                                                     |
| --------------------- | ------------------------------------------------------------ |
| New window            | [`ctrl+shift+enter`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.New-window) (also ⌘+↩ on macOS) |
| New OS window         | [`ctrl+shift+n`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.New-OS-window) (also ⌘+n on macOS) |
| Close window          | [`ctrl+shift+w`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Close-window) (also ⇧+⌘+d on macOS) |
| Resize window         | [`ctrl+shift+r`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Start-resizing-window) (also ⌘+r on macOS) |
| Next window           | [`ctrl+shift+\]`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Next-window) |
| Previous window       | [` ctrl+shift+[ `]                                           |
| Move window forward   | [`ctrl+shift+f`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Move-window-forward) |
| Move window backward  | [`ctrl+shift+b`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Move-window-backward) |
| Move window to top    | [`ctrl+shift+`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Move-window-to-top) |
| Visually focus window | [`ctrl+shift+f7`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Visually-select-and-focus-window) |
| Visually swap window  | [`ctrl+shift+f8`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Visually-swap-window-with-another) |
| Focus specific window | [`ctrl+shift+1`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.First-window), [`ctrl+shift+2`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Second-window) … [`ctrl+shift+0`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Tenth-window) (also ⌘+1, ⌘+2 … ⌘+9 on macOS) (clockwise from the top-left) |

### Other keyboard shortcuts

The full list of actions that can be mapped to key presses is available [here](https://sw.kovidgoyal.net/kitty/actions/).

| Action                      | Shortcut                                                     |
| --------------------------- | ------------------------------------------------------------ |
| Show this help              | [`ctrl+shift+f1`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Show-documentation) |
| Copy to clipboard           | [`ctrl+shift+c`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Copy-to-clipboard) (also ⌘+c on macOS) |
| Paste from clipboard        | [`ctrl+shift+v`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Paste-from-clipboard) (also ⌘+v on macOS) |
| Paste from selection        | [`ctrl+shift+s`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Paste-from-selection) |
| Pass selection to program   | [`ctrl+shift+o`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Pass-selection-to-program) |
| Increase font size          | [`ctrl+shift+equal`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Increase-font-size) (also ⌘++ on macOS) |
| Decrease font size          | [`ctrl+shift+minus`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Decrease-font-size) (also ⌘+- on macOS) |
| Restore font size           | [`ctrl+shift+backspace`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Reset-font-size) (also ⌘+0 on macOS) |
| Toggle fullscreen           | [`ctrl+shift+f11`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Toggle-fullscreen) (also ⌃+⌘+f on macOS) |
| Toggle maximized            | [`ctrl+shift+f10`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Toggle-maximized) |
| Input Unicode character     | [`ctrl+shift+u`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Unicode-input) (also ⌃+⌘+space on macOS) |
| Open URL in web browser     | [`ctrl+shift+e`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Open-URL) |
| Reset the terminal          | [`ctrl+shift+delete`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Reset-the-terminal) (also ⌥+⌘+r on macOS) |
| Edit `kitty.conf`           | [`ctrl+shift+f2`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Edit-config-file) (also ⌘+, on macOS) |
| Reload `kitty.conf`         | [`ctrl+shift+f5`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Reload-kitty.conf) (also ⌃+⌘+, on macOS) |
| Debug `kitty.conf`          | [`ctrl+shift+f6`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Debug-kitty-configuration) (also ⌥+⌘+, on macOS) |
| Open a *kitty* shell        | [`ctrl+shift+escape`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Open-the-kitty-command-shell) |
| Increase background opacity | [`ctrl+shift+a>m`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Increase-background-opacity) |
| Decrease background opacity | [`ctrl+shift+a>l`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Decrease-background-opacity) |
| Full background opacity     | [`ctrl+shift+a>1`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Make-background-fully-opaque) |
| Reset background opacity    | [`ctrl+shift+a>d`](https://sw.kovidgoyal.net/kitty/conf/#shortcut-kitty.Reset-background-opacity) |

## Other tools

### [termpdf.py](https://github.com/dsanson/termpdf.py)

A terminal PDF/DJVU/CBR viewer

### [mdcat](https://github.com/lunaryorn/mdcat)

Display markdown files nicely formatted with images in the terminal

### [ranger](https://github.com/ranger/ranger)

A terminal file manager, with previews of file contents powered by kitty’s graphics protocol.

### [ssh](https://sw.kovidgoyal.net/kitty/kittens/ssh/)

If something went wrong, please add the following line in your `zshrc` or `bashrc`.

```shell
export TERM=xterm # kitty bug
```

## Q&A

Please search the [Frequently Asked Questions](https://sw.kovidgoyal.net/kitty/faq/) carefully before asking and contact TechJI members if needed. 

## Contrbuting

​		If you encounter any problems in using the project, you can [submit an issue](https://github.com/TechJI-2023/kitty/issues/new) or fork this project to submit an pull request. For pull requests, please be sure to have consistent style to existing modules, follow [PEP 8](https://www.python.org/dev/peps/pep-0008/), have clear identifier naming, and have proper comments.

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=TechJI-2023/kitty&type=Date)](https://star-history.com/#TechJI-2023/kitty&Date)
