---
date: 2021-07-25 15:19:06
layout: post
title: "Remove everything in folder in cli"
subtitle:
description:
image:
optimized_image:
category:
tags:
author: rakhleev
paginate: false
---
`rm -rf -- * .[!.]* ..?*`

Each of the three pattern expands to itself if it matches nothing, but that's not a problem here since we want to match everything and rm -f ignored nonexistent arguments.

Note that `.*` would match `..`

### Oh my Zsh

`rm -rf (.|)*`

Again, **this is for Zsh only**.
