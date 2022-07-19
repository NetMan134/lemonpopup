# lemonpopup

This shell script shows details in macOS-like pop-ups about your audio volume, screen backlight, screen brightness, and keyboard brightness using lemonbar, also in the accompaniment it allows you to change these values.

## Usage

> `lemontify -p {audio|bcklight|bright|kbdlight} [-h | -v | -i | -d | -o | -m | -t | -e | -r | -s <val> | -a text]`

| Description			    | Command   |
| :------------------------ | :-------- |
|-h \| --help				| Show this help|
|-v \| --verbose			| Print verbose output|
|-i \| --inc				| Increase current level|
|-d \| --dec				| Decreasse current level|
|-o \| --off				| Set current level to off|
|-m \| --max				| Set current level to max|
|-t \| --toggle			    | Toggle on\|off (if applicable)|
|-e \| --empty			    | Print empty squares (default=false)|
|-r \| --ramp				| Ramp icon based on level (default=false)|
|-l \| --line				| Print as one line (disable multiline)|
|-s \| --step \<value\>		| Set increment\|decrement step|
|-a \| --text \<value\>		| Print additonal output text|
|-p \| --provider \<value\>	| Set the current provider|
|<div style="text-align: right">provider:audio</div>	|Set audio volume (using pactl)|
|<div style="text-align: right">provider:bcklight</div>	|Set screen backlight (using xbacklight)|
|<div style="text-align: right">provider:bright</div>	|Set screen brightness (using xrandr)|
|<div style="text-align: right">provider:kbdlight</div>	|Set keyboard LEDs|


For more information see my reddit post: [here](https://www.reddit.com/r/unixporn/comments/f8mhku/lemonbar_lemontify_osxinspired_notification/) or [direct link to reddit video](https://v.redd.it/wipy5o0l4ti41/DASH_1080?source=fallback)
