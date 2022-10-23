# lemonpopup

This shell script shows notifications in macOS-like (but not only) pop-ups about your adjustable controls level (audio volume, screen backlight, screen brightness, keyboard brightness) using lemonbar, also in the accompaniment allowing to change it.

## Usage

```
lemonpopup  -p <audio|backlight|brightness|kbdlight> \
            [ -evrl ] [ -i <step> | -d <step> | -o | -m | -T ] \
            [ -a <text> ] [ -t <seconds>]
```

<div class="table-wrapper" style="overflow-x: scroll;" markdown="block">
    <table>
        <thead>
            <tr>
                <th colspan="2" style="/*text-align:center;*/" >Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>-h, --help</td>
                <td>Show help menu</td>
            </tr>
            <tr>
                <td>-v, --verbose</td>
                <td>Print verbose output</td>
            </tr>
            <tr>
                <td>-i, --increase &#60;step&#62;</td>
                <td>Increase current level by a step value</td>
            </tr>
            <tr>
                <td>-d, --decrease &#60;step&#62;</td>
                <td>Decrease current level by a step value</td>
            </tr>
            <tr>
                <td>-o, -off</td>
                <td>Set current level to off (lowest applicable)</td>
            </tr>
            <tr>
                <td>-m, --max</td>
                <td>Set current level to max (100% if possible)</td>
            </tr>
            <tr>
                <td>-T, --toggle</td>
                <td>Toggle on or off (if applicable)</td>
            </tr>
            <tr>
                <td>-t, --time &#60;seconds&#62;</td>
                <td>Set duration time</td>
            </tr>
            <tr>
                <td>-e, --empty</td>
                <td>Print empty squares (default=false)</td>
            </tr>
            <tr>
                <td>-r, --ramp</td>
                <td>Ramp icon based on level (default=false)</td>
            </tr>
            <tr>
                <td>-l, --line</td>
                <td>Print as one line (disable multiline)</td>
            </tr>
            <tr>
                <td>-a, --text</td>
                <td>Print additonal output text (still working on it)</td>
            </tr>
            <tr>
                <td>
                    -p, --provider &#60;value&#62;
                    <div style="text-align: right;">
                        <em>audio<br>backlight<br>brightness<br>kbdlight</em>
                    </div>
                </td>
                <td style="position:relative;">
                    <div style="position:absolute; top:5px;">
                        Set the current provider
                    </div>
                    <div style="position:absolute; bottom:5px;">
                        <em>Audio volume (using pactl)<br>Screen backlight (using xbacklight)<br>Screen brightness (using xrandr)<br>Keyboard LED (using kbdlight)</em>
                    </div>
                </td>
            </tr>
        </tbody>
    </table>
</div>

## Dependencies

- [lemonbar-xft-multiline](https://github.com/ibhagwan/bar) - to display the pop-up (@iBhagwan's fork with support for multi-line - if you're not planning to use multiline, you can use an up-to-date original version of [lemonbar](https://github.com/lemonboy/bar), check out the screenshots below to see the difference)
- pactl (essentially PipeWire or PulseAudio) - to change audio level
- xbacklight - to change screen backlight level (if you can control it via cli)
- xrandr - to change screen brightness level
- kbdlight - to change keyboard LED light level (if any)
- font-awesome (font-awesome5?)
- nerd-fonts
- bc
- sed
- awk
- getopt (GNU)

## Screenshots

### Multi-line (macOS-like look)
![multi-line](/screenshots/multi-line-showcase.png)

### Single-line
![single-line-uncompleted](/screenshots/single-line-showcase-uncompleted.png)

## Details

This is a fork of @iBhagwan's [lemontify](https://github.com/ibhagwan/lemontify).<br>
For more information see his [reddit post](https://www.reddit.com/r/unixporn/comments/f8mhku/lemonbar_lemontify_osxinspired_notification/).

### Licensing

Although the original repository does not cover licensing information, @iBhagwan gave me permission to change the code, and re-distribute it - [see here](https://github.com/ibhagwan/lemontify/issues/4#issuecomment-1188837855).<br>
This project is distributed under The Unlicense. For more information, see the [LICENSE](/LICENSE) file.