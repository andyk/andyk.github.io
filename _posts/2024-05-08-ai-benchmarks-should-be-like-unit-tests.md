---
layout: post
title: "AI benchmarks should be like unit tests"
---

Today's go-to LLM benchmarks incentivize model makers to improve marginal
performance on tasks that AIs (i.e., a model or model+memory+tools+etc.) have
already mastered at superhuman-levels like general Q&A, fact recall,
summarization, simple few-step reasoning, etc. In contrast, my favorite
benchmarks are more like unit tests in that they test a skill which AIs still
haven't achieved at human-level, e.g., complex logical inference, tool usage,
long term memory, knowing what they don't know, integrating actions +
observations + reasoning, learning how to learn.

By design, today's best AIs will perform miserably on such a benchmark
(analogous to the unit test failing), which will focus research and engineering
efforts on high-leverage areas of improvement.
[SWE-Bench](https://swebench.com) is a good example (top score on leaderboard
is 12.5%). Can we build benchmarks like this for use-cases beyond software
engineering? Maybe healthcare, finance, data science/eng., personal assistant,
social influencer…?

