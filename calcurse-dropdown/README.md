# calendar

Shows the current date and time. When clicked, a calendar popup is created.

# Dependencies

* calcurse
* Alacritty

# Installation

```ini
[calcurse-dropdown]
command=$SCRIPT_DIR/calcurse-dropdown
interval=1
LABEL= 
DATEFMT=+%H:%M:%S
# SHORTFMT=+%H:%M:%S
```

Add the following to i3 config:
```
for_window [class="Alacritty" title="cal-dropdown"] floating enable, move position 1900 px 35 px, resize set 500 px 500 px
```
