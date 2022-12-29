---
title: Upcoming: FancyVideo-API v3
description: 
published: false
date: 2022-12-29T16:25:54.526Z
tags: 
editor: markdown
dateCreated: 2022-12-29T16:10:11.668Z
---

# Upcoming changes and features
This page lists planned features for future versions of FancyVideo-API.
> Planned features may be delayed or not implemented at all. A ticked box indicates that a feature has been implemented into the current dev branch.
{.is-info}

## Upcoming in v3
- [x] PlayerEvents will get support for statically binding them to a specific player. This will allow replacing 
```java
@FancyVideoEvent()
public void onFinished(PlayerEvents.PlayerFinishedEvent event) {
    if (event.getPlayer() == new DynamicResourceLocation("modid", "playername")) {
        Constants.LOG.info("Finished Event Fired");
        if (event.getMediaPlayer().providesAPI()) {
            event.getMediaPlayer().api().media().play("https://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4");
        }
    }
}
```
with
```java
@FancyVideoEvent(player = "modid:playername")
public void onFinished(PlayerEvents.PlayerFinishedEvent event) {
    Constants.LOG.info("Finished Event Fired");
    if (event.getMediaPlayer().providesAPI()) {
        event.getMediaPlayer().api().media().play("https://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4");
    }
}
```

---

- [ ] The DrawBackgroundEvent might get dropped, as it does not suit all use cases. I'm currently thinking about replacing it with a generous @RenderEvent(String identifier) to provide an easy to use multiloader solution. Mods developed for a single mod loader should switch to the render event provided by the loader.

---

- [ ] Annotate a method with @TimedEvent(int millis) to periodically call the method with the specified interval. This is added to allow easy and resource friendly refreshes of video frames, e.g. for rendering them on a block. 

---

- [ ] Module based: V. 3.0.0 will get split into different packages. There will be the mod, containing the API and several smaller mods providing the required natives. My currently plan for the modules is: Main (The API itself), Core (Containig the minimum required natives as well as a full snappackages), Local (Containing libraries required for local filesystem access. I'm not yet sure if I'm going to integrate those into Core) and Online (Containing plugins for http/s access, as well as third party sites, e.g. Youtube). I decided to do this split, as it allows me to develop the API separated from the natives. It also makes it easier for others to package and provide their own VLC modules.

---

- [ ] Easy Linux support!

---

- [ ] As 3.0.0 will already be a breaking change for every mod using FV-API, I plan to rename the base package from nick1st.* to de.nick1st.* in order to follow naming conventions.

---

- [ ] All versions will be shorted to 3 numbers, e.g 2.2.10.0 -> 3.0.0, as the old versioning caused some problems.

---


<br>

## Upcoming in v4

- [ ] Mac OS support: This should be available as soon as VLC 4.0 is released.

---

- [ ] Integrating the audio from videos into Minecraft's sound engine

---

<br>

## Long term goals being considered

> Goals listed here have a high chance of never being implemented.
{.is-warning}


- [ ] Chrome OS and Android Support
---
- [ ] Providing different native backbones, in a way like the EzMediaCore Plugin does.
---
- [ ] Video Capturing
---