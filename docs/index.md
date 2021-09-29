# Passpartout

Passpartout (not Passepartout) is an avatar generator for [Two Cans and
String](https://twocansandstring.com).

To use, message [Passpartout](https://twocansandstring.com/users/passpartout).

## Synopsis

`IMAGE_URL [ -r RESAMPLE ] [ -i ] [ -f ] [ -m ] [ --background ] [ --palette
PALETTE ] `

## Options

* `-r RESAMPLE`
    * Resampling method. Available values: `NEAREST`, `BILINEAR`, `BICUBIC`,
      `LANCZOS` (default)
* `-i`
    * Inverts the image
* `-f`
    * Flips the image vertically
* `-m`
    * Mirrors the image horizontally
* `--background`
    * Adds a background to the source image. Useful for images with
      transparency
* `--palette PALETTE` or `--palette NUM_COLORS`
    * Can either be the name of a palette or a number which represents the
      number of colors in the palette, based on the colors of the image
    * The maximum value of `NUM_COLORS` is 5
    * Check [the available palettes](#available-palettes) for more palettes


## Examples

Generate a smiley face avatar, resize with Lanczos algorithm:

`https://m.media-amazon.com/images/I/51zLZbEVSTL._AC_SL1200_.jpg`

Generate a smiley face avatar, resize with bicubic interpolation and flip the
image:

`https://m.media-amazon.com/images/I/51zLZbEVSTL._AC_SL1200_.jpg -r BICUBIC -f`

Generate a smiley face avatar with the "Gameboy" palette:

`https://m.media-amazon.com/images/I/51zLZbEVSTL._AC_SL1200_.jpg --palette Gameboy`

# Palettes

The palette of an image can be restricted to a few colors. Passpartout can
generate an avatar using only a select number of colors found in the image or
from the available palettes.

This is especially useful when creating pixel art from your source images or
changing the colorscheme of any existing avatar.

## Available palettes

* Halloween
* Gameboy
* Steel
* Hieroglyph
* Monochrome

## Demonstration

Original:

![](https://twocansandstring.com/uploads/drawn/27538.png)
![](https://twocansandstring.com/uploads/drawn/27516.png)

New:

![](./assets/ebag-gameboy.png)
![](./assets/poodonkus-gameboy.png)

Courtesy of [e-bag](https://twocansandstring.com/users/ebag) and
[Poodonkus913](https://twocansandstring.com/users/poodonkus913)

# Notes

* In palette mode, the image will automatically be resized with both dimensions
  at most 512 pixels. This is to reduce the amount of time processing the
  image.
* For each user, requests are limited to one per minute.
