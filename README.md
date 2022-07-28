# lemonpopup

This shell script shows notifications in macOS-like pop-ups about your adjustable controls level (audio volume, screen backlight, screen brightness, keyboard brightness) using lemonbar, also in the accompaniment allowing to change it.

## Usage

```
lemonpopup  -p <audio|backlight|brightness|kbdlight> \
            [ -evrl ] [ -i <step> | -d <step> | -o | -m | -T ] [ -a <text> ] [ -t <time>]
```

| Description			    | Command   |
| :--------------------     | :-------- |
|-h (--help)		    	| Show this help menu
|-v (--verbose) 	    	| Print verbose output
|-i (--inc)				    | Increase current level
|-d (--dec)			    	| Decreasse current level
|-o (--off)				    | Set current level to off
|-m (--max)			    	| Set current level to max
|-T (--toggle)			    | Toggle on\|off (if applicable)
|-t (--time)		    	| Set duration time
|-e (--empty)		    	| Print empty squares (default=false)
|-r (--ramp)			    | Ramp icon based on level (default=false)
|-l (--line)			    | Print as one line (disable multiline)
|-a (--text) \<text\>	    | Print additonal output text (still working on it)
|-p (--provider) \<value\>  | Set the current provider
|<div style="text-align: right">provider:audio</div>	    |Audio volume (using pactl)|
|<div style="text-align: right">provider:backlight</div>	|Screen backlight (using xbacklight)|
|<div style="text-align: right">provider:brightness</div>	|Screen brightness (using xrandr)|
|<div style="text-align: right">provider:kbdlight</div>	    |Keyboard LED (using kbdlight)|

## Dependencies

- [lemonbar-xft-multiline](https://github.com/ibhagwan/bar) - to display the pop-up (@iBhagwan's fork with support for multiline - if you're not planning to use multiline, you can use an up-to-date original version of [lemonbar](https://github.com/lemonboy/bar))
- pactl - to change audio level
- xbacklight - to change screen backlight level (if you can control it via cli)
- xrandr - to change screen brightness level
- kbdlight - to change keyboard LED light level (if any)
- font-awesome (font-awesome5?)
- nerd-fonts
- bc
- sed
- awk
- getopt (GNU)

## Details

This is a fork of @iBhagwan's [lemontify](https://github.com/ibhagwan/lemontify).<br>
For more information see his [reddit post](https://www.reddit.com/r/unixporn/comments/f8mhku/lemonbar_lemontify_osxinspired_notification/).

### Licensing

Although the original repository does not cover licensing information, @iBhagwan gave me permission to change the code, and re-distribute it - [see here](https://github.com/ibhagwan/lemontify/issues/4#issuecomment-1188837855).<br>
This project is under a MIT License. For more information, see the [LICENSE]() file.