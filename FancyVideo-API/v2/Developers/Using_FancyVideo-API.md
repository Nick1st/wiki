---
title: Using FancyVideo-API in your mod
description: 
published: true
date: 2022-12-29T16:28:36.304Z
tags: fancyvideo-api v2, links missing/broken, work-in-progress
editor: markdown
dateCreated: 2022-12-29T15:42:20.128Z
---

# Getting Started

> This documentation is work-in-progress.
{.is-warning}

To start using FancyVideo-API as a dependency for your mod you need to add it to your `build.gradle`:

```groovy
repositories {
  	maven {
				url "https://maven.nick1st.de/releases"
		}
}

dependencies {
		implementation fg.deobf(implementation "nick1st.fancyvideo:FancyVideo-API-${project.fv_mc_version}:${project.fv_version}")
}
```

> Have a look at the [maven](https://maven.nick1st.de/#/releases/nick1st/fancyvideo) to find valid versions.
{.is-info}

## The MediaPlayer Object

## Custom Events

## Additional Pages
- [Best Practice]
- [I don't know yet]

## Upcomming: FancyVideo-API v3
Have a look at [planned features for v3](/FancyVideo-API/v2/Developers/Upcoming).