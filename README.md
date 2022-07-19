# lemonpopup

This shell script shows details in macOS-like pop-ups about your audio volume, screen backlight, screen brightness, and keyboard brightness using lemonbar, also in the accompaniment it allows you to change these values.

## Usage

```
lemontify   -p { audio | bcklight | bright | kbdlight } \
            [-h | -v | -i | -d | -o | -m | -t | -e | -r | -s <val> | -a text]
```

| Description			| Command   |
| :---------------------| :-------- |
|-h (--help)			| Show this help menu
|-v (--verbose) 		| Print verbose output
|--debug        		| Print debugging information
|-i (--inc)				| Increase current level
|-d (--dec)				| Decreasse current level
|-o (--off)				| Set current level to off
|-m (--max)				| Set current level to max
|-t (--toggle)			| Toggle on\|off (if applicable)
|-e (--empty)			| Print empty squares (default=false)
|-r (--ramp)			| Ramp icon based on level (default=false)
|-l (--line)			| Print as one line (disable multiline)
|-s (--step) \<value\>	| Set increment \| decrement step
|-a (--text) \<value\>	| Print additonal output text
|-p (--provider) \<value\>| Set the current provider
|<div style="text-align: right">provider:audio</div>	|Set audio volume (using pactl)|
|<div style="text-align: right">provider:bcklight</div>	|Set screen backlight (using xbacklight)|
|<div style="text-align: right">provider:bright</div>	|Set screen brightness (using xrandr)|
|<div style="text-align: right">provider:kbdlight</div>	|Set keyboard LEDs|

## Dependencies

- [lemonbar](https://github.com/ibhagwan/bar) - to display the pop-up (@iBhagwan's fork with support for multiline - if you're not planning to use multiline, you can use an up-to-date original version of [lemonbar](https://github.com/lemonboy/bar))
- pactl - to change audio level
- xbacklight - to change screen backlight level
- xrandr - to change screen brightness level

## Details

This is a fork of @iBhagwan's [lemontify](https://github.com/ibhagwan/lemontify).<br>
For more information see @iBhagwan's [reddit post](https://www.reddit.com/r/unixporn/comments/f8mhku/lemonbar_lemontify_osxinspired_notification/).

### License

Although the original repository does not cover licensing information, @iBhagwan gave me permission to change the code, and re-distribute it - [see here](https://github.com/ibhagwan/lemontify/issues/4#issuecomment-1188837855).<br>
This project is under a MIT License. For more information, see the [LICENSE]() file.