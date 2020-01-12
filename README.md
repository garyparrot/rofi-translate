# Rofi translate

Simple rofi script for translation based on [translate shell](https://github.com/soimort/translate-shell)

## Demo

### Brief mode

Brief translation, provide simple translation with pronunciation audio.

![Demo1](./demo/demo1.gif)

### Verbose mode

Provide detail of specific translation

![Demo2](./demo/demo2.gif)

## Requirement

* [rofi](https://github.com/davatorium/rofi)
* [translate shell](https://github.com/soimort/translate-shell)
* mplayer (without it you can't play the audio file)

### Archlinux
``` bash
sudo pacman -S translate-shell rofi mplayer
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

### Usage

shell
``` bash
$ rofi_trans
$ rofi_trans brief
$ rofi_trans verbose
$ rofi_trans delete
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

    # Directory for cache audio files
    export transAudioCacheDir="$HOME/.rofi_trans_audio"

    # target language for translation
    export transTarget="zh-TW"

    # transArgs: Arguement for translate shell
    export transArgs="-b -speak"

    # display some debug information, run it in shell so you can see it
    export verbose="1"

    # auto refresh the content of each mode after every operation, this will cause the rofi flash(close and open)
    export auto_refresh="1"

    export version=1
}
```
