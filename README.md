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
rofi_trans verbose
```

Add key binding for i3-wm
``` plaintext
bindsym $mod+t exec rofi_trans
```

### Configuration of rofi-translate

Open the file ``rofi_trans`` with your text editor.
Then make changes to these environment variables.

```bash
function Configs {
    # the default translation engine for translate-shell.
    export primary_translator="google"

    # the alternative translation engine for translate-shell. Once the primary engine malfunctioned, the secondary engine replace it.
    export secondary_translator="bing"

    # the file use to storing your translating history.
    export transHistory="$HOME/.rofi_trans"

    # target language for translation
    export transTarget="zh-TW"

    # transArgs: Arguement for translate shell
    export transArgs="-b -speak"

    # display some debug information, run it in shell so you can see it
    export verbose="1"

    export version=1
}
```
