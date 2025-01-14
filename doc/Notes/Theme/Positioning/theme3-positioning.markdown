# Positioning Rofi on the monitor

In the current theme format you set these properties on the `window`  widget.

The first, position, determines where **rofi** is placed on the monitor, the
second what point of the **rofi** window connects there. This sounds
complicated, but it ain't.

## position setting

The position setting determines the place of the window on the monitor.

The position setting supports the following values:

 * north
 * northeast
 * northwest
 * south
 * southeast
 * southwest
 * east
 * west
 * center

This is depicted in the diagram below:

![positions](anchors.svg)


## anchor setting

The anchor sets what point of the **rofi** window is placed at the specified *position*.

The *anchor* settings supports the same values as the *position* setting.

If you want the middle of the **rofi** window to be always located at the center of the monitor set both *position* and
*anchor* to `center`.

If the **rofi** window resizes, its center will stay at the center.
If you set the *anchor* to `north` the top of the **rofi** window is at the center of the monitor, and the window will grow
down.

If you set the *anchor* and *position* to `south`, **rofi** is located at the bottom center and the window grows up.

> Note that if you set the *anchor* to `south`  and the *position* to `north` the **rofi** window will be placed above
> the monitor and might not be visible.


> In another blog post we will explain how the dynamic sizing behaviour of **rofi** can be tweaked or disabled.

So the following theme setting will place the top of the **rofi** window in the center of the monitor:

```css
window {
    position: center;
    anchor: north;
}
```

As depicted here, RED is the position (center of screen), GREEN is the position on **rofi** window (north):

![positions](example-pos.png)

> Quick hint, if you want to quickly test out changes to the theme, without editing the file, run **rofi** like:

```bash
rofi -show run -theme-str "window { position: center; anchor: north;}"
```
