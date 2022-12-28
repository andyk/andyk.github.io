---
layout: post
title: "Resources about Reinforcement Learning and Agent Development"
---

Over the last few years I've spent some time reading up on technologies related to building intelligent software agents. I read somewhat broadly but was particularly interested in research at the intersection of neuroscience and AI.

I used the slide deck below to collect excerpts and screen shots, and to take notes as I made my way through my personal survey of related areas so that I could go back and find them easily in the future. The slides are loosely structured into a sort of (very rough) draft course for software developers about building intelligent agents. While the slides include some of my own (mostly incomplete) ideas, they mostly they list and summarize resources from the areas of reinforcement learning (RL), neuroscience, bayesian statistics, cognitive architectures, "production systems", robotics, control theory, behavioral psychology, and markov decision processes (MDPs).

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vRasBVCw_xp5QHbEMIGBBdETHrE5aELqkFa3DJwOUiWX2ZmzYV24c-3w21YWGzyMTtEUBzaXWUhsszu/embed?start=false&loop=false&delayms=3000" frameborder="0" width="100%" height="450" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

To avoid confusion or potential for accidental plagiarism, note that the content of these slides is copied and pasted (or image-captured) directly from the resources that are shown. If in doubt, assume that the text, images, or ideas are not mine but the original authors.

## Other Useful Resources
In case the slides above are too verbose for you, here are direct links to some of the more interesting ones (I think these are all included in the slides).

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
* [List of RL frameworks]({% post_url 2021-02-01-list-of-rl-frameworks %}) - here is a list of Open Source RL development Frameworks.