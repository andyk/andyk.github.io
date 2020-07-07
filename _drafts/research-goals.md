---
layout: post
title: "Research goals"
---

In this post I'll share my research and development goals, and some of my favorite learning resources.

_**Summary:** my main research goal is to build learning agents using techniques from multiple disciplines, including reinforcement learning, cognitive psychology, bayesian statistics, and neuroscience. I also intend to develop open source tools that make my job as an agent developer easier._

## Background
I spent the past year studying reinforcement learning (RL) and related disciplines. When I set out, I wanted to familiarize myself with existing research on software programs that behave with agency and learn. By agency, I mean that the program observes and acts in a world, either a simulated world such as a video game, or the real world the way robots do. As I came up to speed,  

## My research & development goals
I want to contribute to the research and development of learning agents. Specifically, I want to build new agents as well as open source systems that accelerate agent development.

I am focused on agent architectures that leverage techniques from RL, neuroscience, bayesian statistics, cognitive architecture, and production systems. I also want to understand how the human mind encodes agency and learning and then apply that to software agents.

In addition, I am focused on systems that make it easier to build, run, and share learning agents.

## Related work
There is a lot of research available on these topics from many different perspectives, including neuroscience, AI, ML, RL, behavioral psychology, robotics, etc. With so many options to explore, it took me a while to hone in on resources that are relevant to my interests (software, systems, and brains). For example, many papers I've read are focused on algorithms that play Atari games, whereas I'd like to work with agents in a more general environment. Also, many of the textbooks I've read present a formal mathematical framework for understanding learning agents. While I enjoy the math and appreciate, e.g., Markov Decision Processes, I am also keen to find and work on architectures, conventions, and tools more oriented towards software engineers developing agents. 

## Useful resources
Here are some of my favorite learning resources so far:

* [Reinforcement Learning textbook](http://www.incompleteideas.net/book/the-book-2nd.html) by Sutton and Barto, full PDF is available for free online.
    * A classic textbook on the theory of RL. It is math-heavy with pseudocode for most algorithms it covers. The textbook has three parts: (1) tabular solution methods (introduces Bandit algorithms, Dynamic programming, Q-tables, TD), (2) approximate solution methods (introduces function approximation with deep nets for the Q-table, Sarsa, TD-lambda, REINFORCE) (3) a survey of RL applications (psychology, neuroscience, game playing). I enjoyed spending about 6 months reading this textbook and working through the math.
* [Sergey Levine's UC Berkeley Grad level course  on Deep RL](http://rail.eecs.berkeley.edu/deeprlcourse/)
    * The lecture videos are math-heavy with very little code. The homeworks are a good introduction to the basics, though there is a decent amount of boiler plate code to sort through. The last part of the course covers current research topics in RL and the last ~10 lectures of each semester are given by guests active in the field.
* [David Silver's UCL Course on RL](https://www.davidsilver.uk/teaching/) ([youtube playlist](https://www.youtube.com/playlist?list=PLqYmG7hTraZDM-OYHWgPebj2MfCFzFObQ))
    * The lectures are concise and relatively short. I found his explanations useful and appreciated his teaching style.
* The RL chapter (ch18) of [Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow, 2nd edition](https://www.oreilly.com/library/view/hands-on-machine-learning/9781492032632/) by Aurélien Géron
    * He implements a few classic RL algorithms from scratch in python (REINFORCE, DQN, ...) and explains every step of his code. I found it a great starting spot for my own implementations of the classic RL algorithms.
* [How to Build a Brain](https://www.oxfordscholarship.com/view/10.1093/acprof:oso/9780199794546.001.0001/acprof-9780199794546) by Chris Eliasmith
    * This book is a mix of neuroscience and computer science. Eliasmith describes how he and his team designed and implemented a computer agent inspired by the human mind. For example, it sees with an camera and acts with a robotic arm. They built it using biologically realistic simulations of spiking neurons assembled into a task management algorithm modeled after the basil ganglia in the human brain. They also open sourced their development framework [Nengo](https://www.nengo.ai/).
* [The Organisation of Mind](https://www.amazon.com/Organisation-Mind-Tim-Shallice/dp/0199579245) by Shallice and Cooper
     * This book is not computer science oriented. It is about how the brain is organized, drawing on behavioral psychology and neuroscience.
