# About
Bargets is a small set of tiny but nice little widgets to be used in a statusbar, such
as Polybar, i3bar etc.

Where does the name, "bargets", come from? [Bar] Wid[gets].

# Installation
**bargets** requires **python3.10**, so the way to install is:

``` bash
python3.10 -m pip install bargets
```

# Usage
To use a widget in your statusbar, simply provide path to the widget in your
statusbar's config. Make sure to check where **pip** installed the widgets, by
typing `which <widget name>` against any of the widgets, so that you know what
path to use.

### Example: polybar
The following is a snippet of how you could use the battery widget with **polybar**:

``` lua
[battery]
type = custom/script
exec = $HOME/.local/bin/bargets-battery
interval = 5
```

# Configuration: bargets.yaml
If you wish, you can configure each widget how you like in **bargets.yaml**.
First, you need to create a file called **bargets.yaml** to ~/.config/bargets.
You can copy example configuration from
[here](https://github.com/nikkelarsson/bargets/blob/main/examples/bargets.yaml).

# Widgets
| Widget       | Command          |
| -----------: | :--------------- |
| CPU          | bargets-cpu      |
| Battery      | bargets-battery  |

# Requirements
| Requirement  | Note          |
| -----------: | :------------ |
| Python       | 3.10 or higher |
| OS           | MacOS, Linux  |

# Todo
- [ ] Add tests
- [ ] Add command line options
- [ ] Add screenshot(s)
