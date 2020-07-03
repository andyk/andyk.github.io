---
layout: post
title: "Setting up Mycroft on MacOS"
#date: 2020-06-26 14:21:02 -0700
---

Mycroft is an open souce personal assistant, an alternative to Alex, Siri, or OK Google.

Here is what I did to get it working on my 2017 13" MacBook Pro.

Mycroft is written primarily in Python.

To avoid broken links, in case the project files move around in the future, I'm going to reference the most recent commit.

```
git clone git@github.com:MycroftAI/mycroft-core.git

cd mycroft-core
```

First, I read the readme and installation instructions.

Then, I looked at the project layout and how components are organized.

# Architeture
There is a central message bus service [`mycroft-core/mycroft/messagebus/service/`](https://github.com/MycroftAI/mycroft-core/tree/aca6a18c5f408480d1c129d33f2522e7f0c35802/mycroft/messagebus/service). From the code comment in that packages [`__main__.py` file](https://github.com/MycroftAI/mycroft-core/blob/aca6a18c5f408480d1c129d33f2522e7f0c35802/mycroft/messagebus/service/__main__.py):

> "The message bus facilitates inter-process communication between mycroft-core
> processes. It implements a websocket server so can also be used by external
> systems to integrate with the Mycroft system."


Mycroft only supports linux right now, so I poked at its build

```
brew install pulseaudio
