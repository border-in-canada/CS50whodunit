# Questions

## What's `stdint.h`?

stdint.h is a header that contain typedefs for exact bit width integers.

## What's the point of using `uint8_t`, `uint32_t`, `int32_t`, and `uint16_t` in a program?

They allow the programmer to set max/min width values when declaring integers.

## How many bytes is a `BYTE`, a `DWORD`, a `LONG`, and a `WORD`, respectively?

1, 4, 4, 2...respectively.

## What (in ASCII, decimal, or hexadecimal) must the first two bytes of any BMP file be? Leading bytes used to identify file formats (with high probability) are generally called "magic numbers."

It must declare the file type as BM in ASCII or 0x42 0x4D in hex.

## What's the difference between `bfSize` and `biSize`?

bfSize is the size of the entire bitmap file itself, as biSize is the size of the bit info header.

## What does it mean if `biHeight` is negative?

It means that the bitmap is a top-down DIB and its origin is the upper-left corner.

## What field in `BITMAPINFOHEADER` specifies the BMP's color depth (i.e., bits per pixel)?

biBitCount

## Why might `fopen` return `NULL` in lines 24 and 32 of `copy.c`?

 It may return "NULL" if the file is not .bmp specified as the infile or outfile, or other
error at CLI in terms of user input.

## Why is the third argument to `fread` always `1` in our code?

So that it reads the correct number of elements for that specified section of the bitfile (ie. BITMAPINFO HEADER, etc) as defined
by size of parameter.

## What value does line 63 of `copy.c` assign to `padding` if `bi.biWidth` is `3`?

3

## What does `fseek` do?

It sets the file position indicator to an offset determined by, in this case, the size of the padding, so that the padding is
skipped over.

## What is `SEEK_CUR`?

It determinds the current location of the file position indicator.
