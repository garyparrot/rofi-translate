# Rofi translate

Simple rofi script for translation based on [translate shell](https://github.com/soimort/translate-shell)

## Demo

### rofi-verbose

Verbose translation.

![Demo1](./demo/demo1.gif)

### rofi-trans

Speaking on translation, help you with the pronunciation.

![Demo2](./demo/demo2.gif)

## Requirement

* [rofi](https://github.com/davatorium/rofi)
* [translate shell](https://github.com/soimort/translate-shell)

### Archlinux
``` bash
sudo pacman -S translate-shell rofi 
```

## Install
### Download rofi-translate
``` bash
git clone https://github.com/garyparrot/rofi-translate
cd rofi-translate
```

### Configure environment variables
Edit `.xprofile`, add the following line.
``` bash
export PATH=~/rofi-translate:$PATH
```

### Using
shell
``` bash
rofi_trans
```

``` bash
rofi_verbose
```

Add key binding for i3-wm
``` plaintext
bindsym $mod+t exec rofi_trans
```
