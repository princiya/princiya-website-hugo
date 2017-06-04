+++
date = "2017-05-12T17:53:16+02:00"
title = "lf crlf"
tags = [ "lf", "crlf", "file system"]
categories = [ "Technical" ]
series = [ "2017", "May" ]

+++

# Today I Learned - lf & crlf

## Overview

In Unix systems the end of a line is represented with a line feed `LF`. In windows a line is represented with a carriage return (CR) and a line feed (LF) thus `CRLF`. When you get code from git that was uploaded from a unix system they will only have an LF.

## Context

I used one of the existing themes for my HUGO website. Looks like it was from a Unix file system. With my current development environment being Windows, I kept getting the following issue:

`warning: LF will be replaced by CRLF in til/til-example/index.html.`
`The file will have its original line endings in your working directory.`

Although this wasn't the first time I have seen this, I have chosen to ignore this all while. But it was worth learning. I got rid of the warning with the following `git` command:

`git config core.autocrlf false`

More on the above command from git documentation:

![Part 1](/img/lf-1.png)
![Part 1](/img/lf-2.png)

### Source

[This](http://stackoverflow.com/questions/5834014/lf-will-be-replaced-by-crlf-in-git-what-is-that-and-is-it-important) answer from StackOverflow helped me.