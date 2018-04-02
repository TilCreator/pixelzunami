# Pixelzunami
## Draft
### Command TCP sockets
- Normal socket
  - `PX <x> <y> <p|gg|rrggbb|rgb|rrggbbaa|rgba>`  
    Sets pixel. (`p`: 16bit palette, 'gg': Grayscale, 'rrggbb' + 'rgb': red green blue, 'rrggbbaa' + 'rgba': red green blue alpha)
  - `OFFSET <x> <y>`  
    Sets offset for future pixels.
- RX+TX socket
  - `HELP` > `<this>`  
  Returns helpful message.
  - `SIZE` > `<h> <w>`  
  Returns size of display.
  - `PX <x> <y>` > `<rrggbb>`  
  Returns color of pixel.
  - `STATS` > `{'cons': <cons>, 'pps': <pps>(, 'cpp': <cpp>)}`  
  Returns current conections, pps and (cpp (average connections per pixel)) on all sockets as JSON.
- Advanced socket
  - `SC <p|gg|rrggbb|rgb|rrggbbaa|rgba>`  
    Sets pen color (`p`: 16bit palette, 'gg': Grayscale, 'rrggbb' + 'rgb': red green blue, 'rrggbbaa' + 'rgba': red green blue alpha)
  - `PX <x> <y>`  
    Sets pixel with current pen color
  - `OFFSET <x> <y>`  
    Sets offset for future pixels.
- Modification socket  
  Works with tiles, not with pixels:
  One tile is one 1/64 of height and one 1/64 of length, therefore `x` and `y` are in base 64.
  - `INV <xx> <yy>`  
    Inverts the tile.
  - `HUE <xx> <yy> <nn>`  
    Shifts hue at `nn` (hex).
  - // TODO: More commands

### Architecture
// TODO
