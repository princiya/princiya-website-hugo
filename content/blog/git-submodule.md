+++
categories = ["Technical", "May", "2017", "TIL"]
date = "2017-05-11T17:06:54+02:00"
description = "Initialize, update or inspect submodules"
draft = false
tags = ["git"]
title = "git submodule"
weight = 20

+++

A submodule allows you to keep another Git repository in a subdirectory of your repository. The other repository has its own history, which does not interfere with the history of the current repository. This can be used to have external dependencies such as third party libraries for example.

I came across this as I was trying to deploy my Hugo powered website on Github Pages.

The `public` directory from Hugo website is linked to my `princiya.github.io` repository using submodules.
