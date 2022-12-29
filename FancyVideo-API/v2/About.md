---
title: About: FancyVideo-API v2
description: This API provides easy ways for mod developers to play videos in a resource friendly way in Minecraft. 
published: true
date: 2022-12-29T14:45:24.004Z
tags: fancyvideo-api v2, links missing/broken, work-in-progress
editor: markdown
dateCreated: 2022-12-29T13:18:10.259Z
---

# Getting Started

> This documentation is work-in-progress.
{.is-warning}

## For Players
This mod requires some parts of the VLC Media Player. Depending on your operation sytem and architecture (32bit/64bit/arm), you may need to take additional steps to fully install the mod.

> If you can't get the mod working for any reason feel free to ask for help in my [Discord](/FancyVideo-API/v2/About#stay-connected).
{.is-info}

> If there is no suitable VLC build available for your system or you don't want to install VLC, fear not! There won't be any crashes or problems, but videos will be skipped or replaced with a static replacement image.
{.is-info}

> Android and Chrome OS (through PojavLauncher) are currently not supported. Manually installing VLC will not work for those systems.
{.is-danger}


#### Windows
The mod jar comes with bundled librarys for Windows 32bit and 64bit systems. If you're running such a system, you don't need to take any action, the mod will automatically "install" the required files by copying them into your Minecraft profile root folder.

#### Linux
> I am sadly not able to support all Linux distributions. Only Ubuntu based distributions are actively supported. If you get this mod working on other distributions, feel free to [contribute](/FancyVideo-API/v2/About#contribute-to-the-docs) the steps you took.
{.is-warning}

Due to the way native libraries work on linux, you must install a full version of the VLC 4.0 beta. [Download](https://bit.ly/vlcBeta) the VLC <span style="color:yellow;">**4**</span>.0 snap package (or use the Ubuntu PPA as described on the download page) and install it.
The mod should then automatically be able to use it after restarting Minecraft.

#### Mac OS
> Installing the VLC <span style="color:yellow;">**4**</span>.0 beta from this [download page](https://bit.ly/vlcBeta) does work, however Gatekeeper will *warn you about **EVERY** native library loaded **EACH TIME YOU START** Minecraft*. I therfore **DO NOT** recommend fully installing this mod on Mac OS at the time being.
{.is-danger}

If you like tinkering with Mac OS, feel free to ignore the warning above :smile:.

## For Developers
Please have a look at the [Using FancyVideo-API in your mod] page to get started.

## For Modpack Makers
This mod comes with the ability to add replacements in case the native libraries can't be loaded and therefor videos can't be played. However it is up to the mod using this API to correctly implement error handling. In case you run into a crash and think FancyVideo-API is involved, please report this to me via GitHub or Discord.

# Links
- [FancyVideo-API on Curseforge](https://www.curseforge.com/minecraft/mc-mods/fancyvideo-api)
- [FancyVideo-API on Modrinth] <span style="color:red;">A Modrinth page is currently being worked on.</span>
- [FancyVideo-API on GitHub](https://github.com/Nick1st/FancyVideo-API-1.18)
- [Official FancyVideo-API Maven](https://maven.nick1st.de/#/releases/nick1st/fancyvideo)

# Stay Connected
The best and fastest way to get help is to join my [Discord](https://discord.gg/gxcN94H)!

# Contribute to the docs
Contributions to the docs are welcome. Feeel free to open issues and pull requests on [GitHub](https://github.com/Nick1st/wiki).