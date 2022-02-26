<div align="center">

![Python](https://img.shields.io/badge/Python-3.10-informational?style=for-the-badge)
![Release](https://img.shields.io/badge/Release-0.1.0rc2-blueviolet?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

</div>

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

The following is a list of options you can configure in **bargets.yaml**.

| Widget       | Option              | Accepted values     | Description                                  |
| -----------: | :-----------------: | :------------------ | :------------------------------------------- |
| CPU          | unit                | celcius, fahrenheit | Unit to display temperature in.              |
| CPU          | prefix              | any string value    | Text before temperature reading.             |
| CPU          | suffix              | any string value    | Text after temperature reading.              |
| CPU          | indicator           | any string value    | Text between temperature reading and suffix. |
| Battery      | suspend             | true, false         | Suspend computer when charge critically low. |
| Battery      | indicator           | any string value    | Text after battery charge info.              |
| Battery      | threshold.full      | int >90, <=100      | Threshold when battery full.                 |
| Battery      | threshold.low       | int >0              | Threshold when battery low.                  |
| Battery      | threshold.critical  | int >0              | Threshold when battery critical.             |
| Battery      | symbol.discharging  | any string value    | Prefix when battery discharging.             |
| Battery      | symbol.charging     | any string value    | Prefix when battery charging.                |
| Battery      | subject.low         | any string value    | Notification subject on low charge.          |
| Battery      | body.low            | any string value    | Notification body on low charge.             |
| Battery      | subject.full        | any string value    | Notification subject on full charge.         |
| Battery      | body.full           | any string value    | Notification body on full charge.            |

# Widgets
| Widget       | Command          | Description                                                      |
| :----------: | :--------------: | :--------------------------------------------------------------: |
| CPU          | bargets-cpu      | Display CPU's current temperature                                |
| Battery      | bargets-battery  | Display battery charge (%) & state (i.e. charging / discharging) |

# Requirements
| Requirement  | Note          |
| :----------: | :-----------: |
| Python       | 3.10          |
| OS           | MacOS, Linux  |

# Todo
- [ ] Add tests
- [ ] Add command line options
- [ ] Add screenshot(s)
- [x] Add config file examples
