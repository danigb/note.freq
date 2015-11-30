# note.freq

[![Build Status](https://travis-ci.org/danigb/note.freq.svg?branch=master)](https://travis-ci.org/danigb/note.freq)
[![Test Coverage](https://codeclimate.com/github/danigb/note.freq/badges/coverage.svg)](https://codeclimate.com/github/danigb/note.freq/coverage)
[![Climate](https://codeclimate.com/github/danigb/note.freq/badges/gpa.svg)](https://codeclimate.com/github/danigb/note.freq)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat)](https://github.com/feross/standard)
[![npm version](https://img.shields.io/npm/v/note.freq.svg)](https://www.npmjs.com/package/note.freq)
[![license](https://img.shields.io/npm/l/note.freq.svg)](https://www.npmjs.com/package/note.freq)
[![tonal](https://img.shields.io/badge/tonal-note.freq-yellow.svg)](https://www.npmjs.com/browse/keyword/tonal)

`note.freq` is a function (1.3kb minified) to get the frequency from a note name:

```js
var freq = require('note.freq')
freq(440, 'A3') // => 220
```

This is part of [tonal](https://github.com/danigb/tonal)

## Installation

Install via npm: `npm install --save note.freq` or use add the dist file to the html page.

## API

## `note.freq`

Get the pitch frequency in herzs with custom concert tuning

This function is currified so it can be partially applied (see examples)

### Parameters

* `tuning` **`Float`** the frequency of A4 (null means 440)
* `note` **`String or Array`** the note name


### Examples

```js
note.freq(null, 'A4') // => 440
note.freq(444, 'A4') // => 444
```
```js
// partially applied
['A4', 'A#4', 'B5'].map(note.freq(440)) // => [440, ...]
var baroque = note.freq(415)
baroque('A3') // => 207.5
```

Returns `Float` the frequency of the note


## License

MIT License
