# ANSHI [![Version](https://img.shields.io/npm/v/anshi.svg)](https://www.npmjs.com/package/anshi) [![Downloads](https://img.shields.io/npm/dm/anshi.svg)](https://www.npmjs.com/package/anshi)
An easy-to-use ASCI escape code library made by Ashi

## Installation

```
npm install anshi
```


## Usage

```js
const ansi = require('anshi');
// OR
import ansi from 'anshi'

const p = str => process.stdout.write(str);

// move cursor to 2, 1
p(ansi.cursor.to(2, 1));

// to up, one down
p(ansi.cursor.up(2) + ansi.cursor.down(1));
```

## API

### cursor

#### to(x, y)
Set the absolute position of the cursor. `x0` `y0` is the top left of the screen.

#### move(x, y)
Set the position of the cursor relative to its current position.

#### up(count = 1)
Move cursor up a specific amount of rows. Default is `1`.

#### down(count = 1)
Move cursor down a specific amount of rows. Default is `1`.

#### forward(count = 1)
Move cursor forward a specific amount of rows. Default is `1`.

#### backward(count = 1)
Move cursor backward a specific amount of rows. Default is `1`.

#### nextLine(count = 1)
Move cursor to the next line a specific amount of lines. Default is `1`.

#### prevLine(count = 1)
Move cursor to the previous a specific amount of lines. Default is `1`.

#### left
Move cursor to the left side.

#### hide
Hide cursor.

#### show
Show cursor.

#### save

Save cursor position.

#### restore

Restore cursor position.


### scroll

#### up(count = 1)
Scroll display up a specific amount of lines. Default to `1`.

#### down(count = 1)
Scroll display down a specific amount of lines. Default to `1`.


### erase

#### screen
Erase the screen and move the cursor the top left position.

#### up(count = 1)
Erase the screen from the current line up to the top of the screen. Default to `1`.

#### down(count = 2)
Erase the screen from the current line down to the bottom of the screen. Default to `1`.

#### line
Erase the entire current line.

#### lineEnd
Erase from the current cursor position to the end of the current line.

#### lineStart
Erase from the current cursor position to the start of the current line.

#### lines(count)
Erase from the current cursor position up the specified amount of rows.


### clear

#### screen
Clear the terminal screen. (Viewport)


## Credit

This is a fork of [sisteransi](https://github.com/terkelg/sisteransi).


## License

MIT © [frqstbite](https://frqst.site)
