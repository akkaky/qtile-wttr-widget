# qtile wttr widget
Simple weather widget fo [qtile](https://github.com/qtile/qtile) window manager. Weather data provided by [wttr.in](https://github.com/chubin/wttr.in). For customize output data see [One-line output](https://github.com/chubin/wttr.in#one-line-output) format.

## Config example
```
widget.Wttr(
  lang='ru',
  location='Minsk',
  format='%C %t(%f),
  units='m',
)
```
