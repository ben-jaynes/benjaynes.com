---
date: 2026-05-12 00:03
draft: true
tags:
  - "#linux"
title: Gnome Calendar Without Gnome Desktop
---
I have tried many different calendar apps on linux and the one that I have enjoyed the most has been Gnome Calendar. It doesn't have the most features but it can do enough for what I need and integrates well with my self-hosted Radicale instance.

When using Gnome Calendar on a computer without Gnome Desktop (in my case Niri and KDE Plasma as a backup) though, there is one problem. You can install it standalone from most package managers but since the rest of Gnome Desktop is not installed there is no way to add online accounts to the calendar. You should still be able to use it locally fine but I wanted to connect it to my Radicale instance so I can sync it between all of my devices.

Here is the best workaround that I have found to get online accounts working with Gnome Calendar without Gnome Desktop:

1. Install gnome-calendar
```bash
dnf install gnome-calendar
```
2. Install evolution
```bash
dnf install evolution
```
