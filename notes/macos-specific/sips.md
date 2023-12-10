# `sips`

**S**criptable **i**mage **p**rocessing **s**ystem. Image manipulation util.

By default `sips` overwrites input image. Use `-o` (`--out`) to specify different output file path (file name or directory).

## Convert Type

```sh
sips -s format 'jpeg' *.png -o ./converted/
```

Converts all png files in current path to jpeg and place them in subdir `converted` (must exist first).

## Resize

* `sips -z <height> <width> <image>`, ignores aspect ratio. Shorthand for `--resampleHeightWidth`.

* `sips -Z <size> <image>` resizes larger side, preserving aspect ratio. Shorthand for `--resampleHeightWidthMax`.

* `sips --resampleWidth <pixels> <image>` resizes width, preserving aspect ratio (similarly for `--resampleHeight`).

## Crop

`sips -c <height> <width> <image>` crops image to given dimensions (relative to center of original image). Shorthand for `--cropToHeightWidth`.

## Rotate

`sips -r <degrees> <image>` rotates image by specified degrees. Shorthand for `--rotate`.

## Flip

```sh
-f horizontal|vertical
--flip horizontal|vertical
```
