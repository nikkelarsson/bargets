# About
Bargets is a small set of tiny but nice little widgets to be used in a statusbar, such
as Polybar, i3bar etc.

Where does the name, "bargets", come from? [Bar] Wid[gets].

# Installation
``` bash
pip install bargets
```

# Usage
To use a widget in your statusbar, simply provide path to the widget in your
statusbar's config. Make sure to check where **pip** installed the widgets, by
typing `which <widget name>` against any of the widgets, so that you know what
path to use. Let's assume that **pip** installed the widgets into `$HOME/.local/bin`.
If you're using **polybar** and you'd like to use the **battery** widget, then
you'd do the following in **polybar's** config:

``` lua
[battery]
type = custom/script
exec = $HOME/.local/bin/bargets-battery
interval = 5
```

# Widgets
| Widget       | Command          |
| -----------: | :--------------- |
| CPU          | bargets-cpu      |
| Battery      | bargets-battery  |

# Requirements
| Requirement  | Note          |
| -----------: | :------------ |
| Python       | 3.8 or higher |
| OS           | MacOS, Linux  |
