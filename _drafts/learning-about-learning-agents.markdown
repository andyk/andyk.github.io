---
layout: post
title: "Learning about learning agents"
---

I've spent about a year so far studying and thinking about learning agents and the algorithms they use, with an emphasis on Reinforcement Learning. My goal when I set out was to familiarize myself with existing research about software programs that behave with agency and learn. By agency, I mean that the program must observe and act in a world, either a simulated world such as a video game, or the real world the way robots do. Along the way I also want to contribute to research and development of more general versions of today's software learning agents. I am specifically interested in the systems that might make it easier to build, run, and share such learning agents and their components. Finally, I'm curious how the human mind encodes agency and learning since perhaps we can apply that to our software agents.

There is much research available on these topics, done from many different perspectives, including neuroscience, AI, ML, RL, behavioral psychology, robotics, etc. With so many options to explore, it has taken me a while to hone in on resources that are relevant to my interests (software, systems, and brains). For example, many papers I've read are focused on algorithms that play Atari games, while I'd like to work with agents in a more general environment. Also, many of the textbooks I've read present a formal mathematical theoretical framework for modeling and understanding learning agents. While I enjoy the math and appreciate, e.g., Markov Decision Processes, I am also keen to find and work on models, architectures, conventions, and tools more oriented towards software engineers developing agents. 


**If I could go back a year, here are some tips I'd give myself:**

* Mix learning and practicing. I primarily learn by reading, watching videos, taking online classes, and study groups. I practice by coding. I've found a 1:1 ratio of the two (by time spent) works pretty well for me.
* Regularly take time to review historical or seminal research and read classic papers.
* Find folks to collaborate with.
    * For academics this is relatively straight-forward, e.g., PhD students have their advisors and other students.
    * ...but we aren't all academics, so use other ways to find your learning buddies: attend meetups, post to slack channels and mailing lists of popular projects, go to conferences, etc.
    * I collaborate closely with [Nick Jalbert](https://nickjalbert.github.io/), mostly through weekly video chats and occasionally in-person mini-retreats.
* Once you find a collaborator...
    * Start reading and discussing. Every few weeks, Nick and I pick a paper or textbook chapter, usually a classic or highly cited paper, read it, and meet to discuss.
    * Code on RL agents together. We do this in all sorts of ways, sometimes we are both working on our own separate implementation of an algorithm that we're focused on, sometimes we give each other code or design reviews, sometimes we pair program.
    * Take an online class together. We are self-studying our way through [Gilbert Strang's online linear algebra course](https://ocw.mit.edu/courses/mathematics/18-06sc-linear-algebra-fall-2011/), etc.
    * Prepare a talk together. We built a short hands-on [Intro to RL tutorial](https://www.meetup.com/LA-Deep-RL/events/268096321/) for the LA Deep RL meetup group.


**And here are some of my favorite learning resources so far:**

* [Reinforcement Learning textbook](http://www.incompleteideas.net/book/the-book-2nd.html) by Sutton and Barto, full PDF is available for free online.
    * A classic textbook on the theory of RL. It is math-heavy with pseudocode for most algorithms it covers. The textbook has three parts: (1) tabular solution methods (introduces Bandit algorithms, Dynamic programming, Q-tables, TD), (2) approximate solution methods (introduces function approximation with deep nets for the Q-table, Sarsa, TD-lambda, REINFORCE) (3) a survey of RL applications (psychology, neuroscience, game playing). I enjoyed spending about 6 months reading this textbook and working through the math.
* [Sergey Levine's UC Berkeley Grad level course  on Deep RL](http://rail.eecs.berkeley.edu/deeprlcourse/)
    * The lecture videos are math-heavy with very little code. The homeworks are a good introduction to the basics, though there is a decent amount of boiler plate code to sort through. The last part of the course covers current research topics in RL and the last ~10 lectures of each semester are given by guests active in the field.
* [David Silver's UCL Course on RL](https://www.davidsilver.uk/teaching/) ([youtube playlist](https://www.youtube.com/playlist?list=PLqYmG7hTraZDM-OYHWgPebj2MfCFzFObQ))
    * The lectures are concise and relatively short. I found his explanations useful and appreciated his teaching style.
* The RL chapter (ch18) of [Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow, 2nd edition](https://www.oreilly.com/library/view/hands-on-machine-learning/9781492032632/) by Aurélien Géron
    * He implements a few classic RL algorithms from scratch in python (REINFORCE, DQN, ...) and explains every step of his code. I found it a great starting spot for my own implementations of the classic RL algorithms.
* [How to Build a Brain](https://www.oxfordscholarship.com/view/10.1093/acprof:oso/9780199794546.001.0001/acprof-9780199794546) by Chris Eliasmith
    * This book is 2 parts neuroscience and 1 part computer science. Eliasmith's group at Waterloo has built a computer agent with a perception/actuation system inspired by the human equivalent (sees with an eye, acts with a robotic arm) using biologically realistic simulations of spiking neurons assembled into a task management algorithm modeled after the human brain's equivalent mechanisms (mostly in the basil ganglia). They also open sourced their development framework [Nengo](https://www.nengo.ai/).
* [The Organisation of Mind](https://www.amazon.com/Organisation-Mind-Tim-Shallice/dp/0199579245) by Shallice and Cooper
     * This book is not computer science oriented. It is about how the brain is organized, drawing on behavioral psychology and neuroscience.
