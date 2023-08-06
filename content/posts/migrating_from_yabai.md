---
title: Migrating from yabai and using ⌥ to focus desktops
date: 2023-08-06
---

I have been using [yabai](https://github.com/koekeishiya/yabai/) for some time as my tiling window manager of choice in macOS.
It works well and has some nice features, like removing the transition animation between desktops.
The problem is some of those features are implemented in a rather clever way that requires partially disabling System Integrity Protection:

> yabai can be installed via Homebrew from a custom tap.
> It does, however, require you to partially disable System Integrity Protection ("rootless"), because it controls windows by acting through Dock.app — which is the sole owner of the main connection to the window server.

This disabled some features like running iOS and iPadOS apps on macOS.
This approach is also prone to breaking whenever a new major OS update is relased, as it is the case with the future version, macOS Sonoma.

For that reason I have decided to stop using yabai and start using [Amethyst](https://github.com/ianyh/Amethyst/) instead.
Amethyst is another tiling window manager for macOS.
Its feature set is more limited than yabai, but all of them work without disabling SIP.

In the end, the features Amethyst provides are provided by yabai without having to disable SIP, so I could have just stayed using Amethyst.

# Focusing a desktop with the ⌥ key

One thing in common to most tiling window managers is the ability to have multiple virtual desktops and have key combinations to easily switch between them.
A common practice is to have each desktop assigned to a number and have a key combination with the corresponding number to switch to that desktop.

In my case I was used to using the ⌥ (or "alt") key together with a number to switch to a certain desktop.
This is natively supported by macOS and it is a feature Amethyst does not provide (yabai does, though). 
In the macOS settings, you can set a keyboard shortcut to switch to the desired desktop. 
I tried to configure it in the same way as before, using the ⌥ key.
However, the problem is that macOS does not differentiate between the left and right ⌥ keys, which prevented me from typing some symbols like "@" or "#".
Other tools like [skhd](https://github.com/koekeishiya/skhd) or [Karabiner Elements](https://karabiner-elements.pqrs.org) do allow you to differentiate between the left and right keys.
What I ended up doing in the end is configuring the shortcuts with the ⇧^⌥⌘ keys and configuring Karabiner to make the left "alt" key act as all of those keys at once.
Problem solved, now I can use the left ⌥ along with a number to switch to the desired desktop, and the right ⌥ key with a number to write the corresponding symbol.
