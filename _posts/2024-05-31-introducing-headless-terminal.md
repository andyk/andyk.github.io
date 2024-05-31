---
layout: post
title: "Introducing Headless Terminal"
---

Introducing *[Headless Terminal (`ht`)](https://github.com/andyk/ht)* - making terminals easy for LLMs to use.

I've been using LLM agents for coding, and needed something like a headless browser but for terminals. So I teamed up with [@sickill](https://x.com/sickill) (creator of [asciinema](https://asciinema.org)) to build [ht](https://github.com/andyk/ht).

Headless Terminal is an open source executable that wraps and provides text screenshots of a terminal. Terminals are one of the oldest and most prolific UI frameworks in all of computing. And they are stateful so, for example, when you use an editor in your terminal, the terminal has to manage state about the cursor location. Without `ht`, an agent struggles to manage this state directly. With ht, an agent can just observe the terminal like a human does.

How `ht` works:

* The ht binary wraps an arbitrary other binary (e.g. bash, vim, etc.) with a VT100 style terminal interface.
* By default, vt will start bash, but you can override it to wrap whatever binary you like (e.g., `ht nano`)
* Communication with ht is performed via stdin, stdout and stderr.
* ht uses simple JSON-based protocol for sending input to its stdin and fetching screenshots of the terminal.
  * Input is sent as a JSON object in the form { "type": "input", "payload": "ls\r" }
  * The agent can "look at" the terminal, i.e., grab a screenshot, by sending the following to JSON object: { "type": "getView" }
* Diagnostic messages (notices, errors) are printed to stderr.

ht is Apache licensed, built in rust, and works on MacOS and Linux.

<center><img src="/assets/img/headless-terminal.png" style="width: 85%" /></center>
