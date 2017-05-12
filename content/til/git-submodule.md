+++
date = "2017-05-11T17:06:54+02:00"
title = "git submodule"

+++

# Today I Learned - git submodule

git-submodule - Initialize, update or inspect submodules

## Overview

A submodule allows you to keep another Git repository in a subdirectory of your repository. The other repository has its own history, which does not interfere with the history of the current repository. This can be used to have external dependencies such as third party libraries for example.

## Context

I came across this as I was trying to deploy my Hugo powered website on Github Pages.

The `public` directory from Hugo website is linked to my `princiya.github.io` repository using submodules.
