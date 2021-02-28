# qtile wttr widget

Simple weather widget for [qtile](https://github.com/qtile/qtile) window
manager. Weather data provided by [wttr.in](https://github.com/chubin/wttr.in).

## Config

Examlpe:

```
Wttr(
    lang='ru',
    location={
        'Minsk': 'Minsk',
        '64.127146,-21.873472': 'Reykjavik',
        '~Vostok Station': 'Nice place',
    },
  format='%l: %C, temp: %t, feels: %f',
  units='m',
  update_interval=30,
)
```

### format

Choose presets in range 1-4 (Ex. `'1'`) or build your own custom output format,
use the special %-notation.
See https://github.com/chubin/wttr.in#one-line-output

### location

Key is a city or place name, or GPS coordinates. Value is a display name. Add
the character `~` at the beginning to get weather for some special location:
`~Vostok Station` or `~Eiffel Tower`. Also can use IP-addresses (direct) or
domain names (prefixed with `@`) to specify a location: `@github.com`,
`123.456.678.123`. Specify multiple locations as dictionary:

```
location={
  'Minsk': 'Minsk',
  '64.127146,-21.873472': 'Reykjavik',
  '~Vostok Station': 'Nice place',
 } 
```

Cities will change randomly every update.

### lang

Set prefered display language. Example: `lang='ru'`.
[More](https://wttr.in/:translation) about supported languages.

### units

`'m'` - metric, `'M'` - show wind speed in m/s, `'s'` - imperial.

### update_interval

Update interval in seconds. Default is `600`. Recommendation: if you want to
display multiple locations alternately, maybe set a smaller interval, ex. `30`.
