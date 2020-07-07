---
layout: post
title: "Setting up Mycroft on MacOS"
id: 20200706133608
#date: 2020-06-26 14:21:02 -0700
---
Mycroft is an open souce personal assistant, an alternative to Alex, Siri, or OK Google.

These are my notes about the system and what I did to get it working on my 2017 13" MacBook Pro.

Mycroft is written primarily in Python.

```
git clone git@github.com:MycroftAI/mycroft-core.git

cd mycroft-core
```

First, I read the readme and installation instructions.

Then, I looked at the project layout and how components are organized.

# Architeture
There is a central message bus service [`mycroft/messagebus/service/`](https://github.com/MycroftAI/mycroft-core/tree/aca6a18c5f408480d1c129d33f2522e7f0c35802/mycroft/messagebus/service). 

> "The message bus facilitates inter-process communication between mycroft-core
> processes. It implements a websocket server so can also be used by external
> systems to integrate with the Mycroft system." -- [`__main__.py`](https://github.com/MycroftAI/mycroft-core/blob/aca6a18c5f408480d1c129d33f2522e7f0c35802/mycroft/messagebus/service/__main__.py).


Mycroft only supports linux right now, so I poked at its installation script [`dev_setup.sh`](https://github.com/MycroftAI/mycroft-core/blob/aca6a18c5f408480d1c129d33f2522e7f0c35802/dev_setup.sh) to see how much work it would be to get the core components of it running on my Mac.

So no good.

Ok that seems to work, but I want the STT and TTS to work.

```
brew install pulseaudio
```
