+++
date = "2017-05-12T20:02:26+02:00"
title = "lf vs cr"

+++

# Today I Learned - lf vs  cf

## Overview

It's really just about which bytes are stored in a file.

## Context

Follow-up on my earlier [post]({{< relref "til/lf-crlf.md" >}}), I wanted to find out what exactly is the difference between the two - `LF` vs `CR`.

`CR` is a bytecode for carriage return (from the days of typewriters) and `LF` similarly, for line feed. It just refers to the bytes that are placed as end-of-line markers.

`CR` is coded as `0x0D (13 decimal)` and `LF` as `0x0A (10 decimal)`.

The two expressions have their roots in the old typewriters / [TTY](http://www.abouttty.com/Whatis.html). LF moved the paper up (but kept the horizontal position identical) and CR brought back the "carriage" so that the next character typed would be at the leftmost position on the paper (but on the same line).

The `End of Line (EOL)` or `CR + LF` sequence `(0x0D 0x0A, \r\n)` is actually two ASCII characters, a combination of the CR and LF characters. It moves the cursor both down to the next line and to the beginning of that line. This character is used as a new line character in most other non-Unix operating systems including Microsoft Windows, Symbian OS and others.

### Sources

* [1](http://stackoverflow.com/questions/1552749/difference-between-cr-lf-lf-and-cr-line-break-types)
* [2](https://en.wikipedia.org/wiki/Newline)