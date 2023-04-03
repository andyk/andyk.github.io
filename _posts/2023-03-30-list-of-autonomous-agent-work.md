---
layout: post
title: "List of Autonomous LLM Agent Projects"
---

This is my scratchpad of interesting projects and products focused on taking LLMs and giving them the ability to do things. There is also a short summary of each project.

* [Toolformer](https://arxiv.org/abs/2302.04761), Timo Schick et al., Meta AI Research, Universitat Pompeu Fabra
* [ReAct - Reasoning + Actions](https://ai.googleblog.com/2022/11/react-synergizing-reasoning-and-acting.html), Shunyu Yao et al., Google Brain
* [MERKL - Modular Reasoning, Knowledge and Language](https://www.ai21.com/blog/jurassic-x-crossing-the-neuro-symbolic-chasm-with-the-mrkl-system), AI21
* [PAL - Program Aided Language Models](https://arxiv.org/abs/2211.10435), Luyu Gao et al., CMU
* [LangChain Agents](https://python.langchain.com/en/latest/modules/agents.html), Harrison Chase
* [GPT Plugins](https://openai.com/blog/chatgpt-plugins), OpenAI
* [Dust](https://dust.tt/), Stanislas Polu
* [DSP - Demonstrate Search Predict](https://github.com/stanfordnlp/dsp/), Omar Khattab et al., Stanford 
* [Reflexion](https://arxiv.org/abs/2303.11366), Northeastern, MIT
* [Auto-GPT](https://github.com/Torantulino/Auto-GPT), Toran Bruce Richards

**Related reads (no code or project per se):**
* [Large Language Models are Zero-Shot Reasoners](https://arxiv.org/abs/2205.11916) - the “let's think step by step” paper, Kojima et al., The University of Tokyo, Google
* [The Near Future of AI is Action-Driven](https://jmcdonnell.substack.com/p/the-near-future-of-ai-is-action-driven?sd=pf), James McDonnell 
* [Sparks of Artificial General Intelligence Early experiments with GPT-4](https://arxiv.org/pdf/2303.12712.pdf) Section 5: "Interaction with the world" (page 43), Seb́astien Bubeck et al., Microsoft
* [Task-driven Autonomous Agent](https://twitter.com/yoheinakajima/status/1640934493489070000), Yohei Nakajima


Most of the summaries below were generated by the [perplexity.ai](https://perplexity.ai) [Chrome extension](https://chrome.google.com/webstore/detail/perplexity-ask-ai/hlgbcneanomplepojfcnclggenpcoldo).

### Toolformer

**[Toolformer: Language Models Can Teach Themselves to Use Tools](https://arxiv.org/pdf/2302.04761.pdf)**, Timo Schick et al., Meta AI Research, Universitat Pompeu Fabra

The paper introduces a new fine-tuned model called Toolformer, which is trained to use external tools via simple APIs in a self-supervised way. The model decides which APIs to call, when to call them, what arguments to pass, and how to best incorporate the results into future token prediction. The model incorporates a range of tools, including a calculator, a Q&A system, a search engine, a translation system, and a calendar. Toolformer achieves substantially improved zero-shot performance across a variety of downstream tasks, often competitive with much larger models, without sacrificing its core language modeling abilities.

### ReAct

**[ReAct: Synergizing Reasoning and Acting in Language Models](https://arxiv.org/pdf/2210.03629.pdf)**, Shunyu Yao et al., Google Brain

The paper discusses the use of large language models (LLMs) to generate both reasoning traces and task-specific actions in an interleaved manner, allowing for greater synergy between the two. The authors apply their approach, named ReAct (for Reasoning + Action), to a diverse set of language and decision-making tasks and demonstrate its effectiveness over state-of-the-art baselines in addition to improved human interpretability and trustworthiness. Specifically, on question answering and fact verification tasks, ReAct overcomes prevalent issues of hallucination and error propagation in chain-of-thought reasoning by interacting with a simple Wikipedia API, and generating human-like task-solving trajectories that are more interpretable than baselines without reasoning traces. Furthermore, on two interactive decision-making benchmarks, ReAct outperforms imitation and reinforcement learning methods by a significant margin.

### MERKL
**[Jurassic-X: Crossing the neuro-symbolic chasm with the MRKL system](https://www.ai21.com/blog/jurassic-x-crossing-the-neuro-symbolic-chasm-with-the-mrkl-system)**, AI21

MRKL (Modular Reasoning, Knowledge and Language) is a system designed to bridge the gap between symbolic reasoning and neural networks. The system uses a DNN to classify incoming messages and creating a plan for a series of calls to expert modules, for examples extracting information from multiple sources and summarizing them. They have built modules for using a database, a calculator, etc. AI21 has a proprietry implementation of the MRKL system, called Jurassic-X, which is being piloted by a few partners.

### PAL: Program-aided Language Models

**[PAL: Program-aided Language Models](https://arxiv.org/pdf/2211.10435.pdf)**, Luyu Gao et al., CMU

The paper presents a new approach called Program-Aided Language models (PAL) that uses large language models (LLMs) to read natural language problems and generate programs as intermediate reasoning steps, but delegates the solution step to a runtime such as a Python interpreter. The authors demonstrate that this approach leads to more accurate results than other methods, including chain-of-thought, on 13 mathematical, symbolic, and algorithmic reasoning tasks. The paper argues that while LLMs are adept at step-by-step decomposition, they often make logical and arithmetic mistakes in the solution part. PAL addresses this issue by using the LLM to generate programs and offloading the solution step to an interpreter. The authors provide code and data publicly.

### LangChain Agents

**[LangChain Agents docs](https://python.langchain.com/en/latest/modules/agents/getting_started.html)**, Harrison Chase & Open Source contributors. The summary below was copied and tweaked from one of [Harrison's tweet threads](https://twitter.com/hwchase17/status/1595456660507459585).

In Langchain, Agents use an LLM to determine which which actions to take and in what order. An action can either be using a tool and observing its output, or returning to the user. "Tools" in this context can be anything that takes a string as input and outputs a string. This can be a search engine, a database, another LLM, a chain, or event another agent.

The abstractions in Langchain were inspired by much of the above work. In the tweet thread linked above, Harrison Chase said "This is NOT a new idea, just a reframing":

> I would argue that @ShunyuYao12's ReAct paper (<https://arxiv.org/pdf/2210.03629.pdf>) uses an agent, which has a "Search" tool and a "Lookup" tool available

> Likewise, I would argue that @OfirPress's self-ask paper (<https://arxiv.org/abs/2210.03350>) uses an agent, which has a "Search" tool available 

> The MRKL implementation (inspired by @AI21Labs [ai21.com/blog/jurassic-x…](https://www.ai21.com/blog/jurassic-x-crossing-the-neuro-symbolic-chasm-with-the-mrkl-system)) is extremely close to this current agent abstraction

### GPT Plugins

**[GPT Plugins](https://openai.com/blog/chatgpt-plugins)**, OpenAI

Plugins aim to be the "eyes and ears" for language models, giving them access to information that is too recent, too personal, or too specific to be included in the LLM's training data. They can also enable language models to perform actions on behalf of users. 

Plugin developers expose one or more API endpoints, accompanied by a standardized manifest file (hosted at `yourdomain.com/.well-known/ai-plugin.json`) and an [OpenAPI specification](https://swagger.io/specification/). Then ChatGPT (or some other AI model) acts as an intelligent API caller, given an API spec and a natural-language description of when to use the API. To build a plugin, developers need to create a manifest file, register the plugin in the ChatGPT UI, and have users activate the plugin. When a user asks a relevant question, the model may choose to invoke an API call from the plugin if it seems relevant, and incorporate the API results into its response to the user.

The features were initially relased as a private beta that required users to joint a waitlist. The first plugins were created by a handful of popular web companies including as Slack, Wolfram, and Zapier. OpenAI is also hosting two plugins themselves: a web browser and code interpreter. Besides the initial plugins, there is also a lugin API that allows anyone to create their own plugins.

## Dust

**[Dust](https://github.com/dust-tt/dust)** ([hosted version](https://dust.tt/)) ([docs](https://docs.dust.tt/overview)), Stanislas Polu & open source contributors

The Dust Platform is a framework (written in Rust) designed to define and deploy large language model apps without writing any execution code. It aims to ease the process of working on multiple examples at the same time, introspecting model outputs produced by intermediary steps of large language model apps, and iterating on the design of large language model apps by providing a granular and automated versioning system. Dust apps are composed of blocks executed sequentially, and each block has a set of specification arguments and configuration arguments. The input block is the block that receives the arguments required to run a Dust app, and Dust apps can also define datasets which are arrays of JSON objects. The Dust execution engine will run an app in parallel on each element attached to the input block.

### DSP

**[Demonstrate-Search-Predict: Composing retrieval and language models for knowledge-intensive NLP](https://github.com/stanfordnlp/dsp/)** ([paper](https://arxiv.org/abs/2212.14024))

The Demonstrate-Search-Predict (DSP) framework is a programming abstraction for building AI systems for knowledge-intensive tasks such as answering user questions or researching complex topics. DSP programs are written in a few lines of code, describing how the problem should be decomposed into smaller transformations. The framework provides primitives for composing transformations and and mapping these transformations to effective language model (LM, GPT-3.5 in this case) and retrieval model (RM - ColBERTv2) calls. DSP discourages "prompt engineering" and offers a number of automatic tuning features. The evaluation in the paper shows DSP beat vanilla GPT-3.5 on Open-SQuAD by 120% (i.e., DSP got a score of 36.6 vs. vanilla GPT-3.5 with a few-shot prompt's score of 16.2). THey beat the simpler Retreive-then-read paradigm by a more modest 8%. They also evaluate performance on HotPotQA, and QReCC. The framework is open source and available for installation and comes with an intro notebook and compiler notebook.

### Reflexion

**[Reflexion: an autonomous agent with dynamic memory and self-reflection](https://arxiv.org/abs/2303.11366)**

Snippet from the abstract: Building on recent research, we propose Reflexion, an approach that endows an agent with dynamic memory and self-reflection capabilities to enhance its existing reasoning trace and task-specific action choice abilities. To achieve full automation, we introduce a straightforward yet effective heuristic that enables the agent to pinpoint hallucination instances, avoid repetition in action sequences, and, in some environments, construct an internal memory map of the given environment. To assess our approach, we evaluate the agent's ability to complete decision-making tasks in AlfWorld environments and knowledge-intensive, search-based question-and-answer tasks in HotPotQA environments. We observe success rates of 97% and 51%, respectively


### End note

Email me (or create a [PR](https://github.com/andyk/andyk.github.io/blob/master/_posts/2023-03-30-list-of-autonomous-agent-work.md)) with anything that I'm missing and I'll update this page.