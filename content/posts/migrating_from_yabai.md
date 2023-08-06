---
title: Migrating from yabai and using ⌥ to focus desktops
date: 2023-08-06
---

I have been using [yabai](https://github.com/koekeishiya/yabai/) for some time as my chosen tiling window manager on macOS.
It works well and has nice features, such as disabling transition animations between desktops.
However, some of these features are implemented in a clever but hackish way and [require partially disabling System Integrity Protection (SIP)](https://github.com/koekeishiya/yabai/wiki/Disabling-System-Integrity-Protection):

> yabai can be installed via Homebrew from a custom tap.
> It does, however, require you to partially disable System Integrity Protection ("rootless"), because it controls windows by acting through Dock.app — which is the sole owner of the main connection to the window server.

Disabling SIP has consequences, such as the inability to run iOS and iPadOS apps on macOS.
Additionally, this approach may break with future macOS updates [like Sonoma](https://github.com/koekeishiya/yabai/issues/1772).

Due to these limitations, I decided to switch from yabai to [Amethyst](https://github.com/ianyh/Amethyst/), another tiling window manager for macOS.
While it has a more limited feature set compared to yabai, all of its features work without disabling SIP.

Ultimately, I realized that the features offered by Amethyst are similar to what yabai does when SIP is disabled. Therefore, I could have continued using yabai. Well, I suppose change is good!

## Focusing a desktop with the ⌥ key

Most tiling window managers allow you to have multiple virtual desktops and switch between them using key combinations. Typically, each desktop is assigned a number, and pressing a specific key combination with that number switches to the corresponding desktop.

Previously, I used the ⌥ (or "alt") key along with a number to switch to a specific desktop.
This is a native feature in macOS but not provided by Amethyst (although yabai does provide it).
In macOS settings, you can set a keyboard shortcut to switch to the desired desktop.
I tried configuring it with the ⌥ key as before, but macOS does not differentiate between the left and right ⌥ keys.
This prevented me from typing certain symbols like "@" or "#".

Fortunately, tools like [skhd](https://github.com/koekeishiya/skhd) or [Karabiner Elements](https://karabiner-elements.pqrs.org) allow you to differentiate between the left and right keys.
In the end, I configured the shortcuts using the ⇧^⌥⌘ keys and used Karabiner to make the left "alt" key act as all of those keys simultaneously.
This solution solved the problem, allowing me to use the left ⌥ key with a number to switch to the desired desktop and the right ⌥ key with a number to type the corresponding symbol.
