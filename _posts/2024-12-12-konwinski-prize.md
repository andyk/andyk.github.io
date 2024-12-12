---
layout: post
title: "Konwinski Prize"
---

Last night, I tweeted on stage at NeurIPS that I’ll give $1 million to the open source AI that breaks 90% on a sweet new version of my favorite benchmark, [SWE-bench](http://swebench.com). It’s called the [Kprize](http://kprize.ai)\!

\<kprize-launch-on-stage.jpg\>  
Left to right: Kaggle CEO [D. Scully](https://scholar.google.com/citations?hl=en&user=l_O64B8AAAAJ&view_op=list_works&sortby=pubdate), SWE-bench creators [Carlos Jimenez](https://www.carlosejimenez.com/) & [John Yang](https://john-b-yang.github.io/); and me

\<kprize-tweet-from-stage\>

Why start with SWE-bench? Well, I fell in love with SWE-bench the moment I saw it. What a great idea: have AI solve real issues from popular GitHub repos. I love that SWE-bench is hard, built from real world data, and measures something that I care about (coding).

The Kprize aims to:

1. Measure how AI coders *really* perform   
2. Model a better way to benchmark  
3. Inspire more people to participate in moving AI forward in the open

Why make a contamination free version of SWE-bench? SWE-bench publishes its test set, like many benchmarks today. This allows those who compete in the benchmark to overfit their solutions. Even if they didn’t officially publish the test set, SWE-bench is composed of issues and code scraped from public GitHub repos, and most models today are trained extensively on code in those same repositories (and just about everything else on the internet) so contamination is a big problem. I've always wondered how the leaderboard would change if the test set weren’t public. That’s why I decided to build a contamination-free version of SWE-bench?

Why will cash only be awarded to submissions that use open source code and open weight models? I am passionate about open source\! One of the things I love most about open source is how it taps into a bigger community energy \- individuals building off the work of other individuals to do something big. I love that feeling of getting swept up into something much bigger than yourself. That moment when you look at your team and say, “*whoa, are we actually doing this?*” That’s how I felt when I was working on Spark at Berkeley, and that’s how I hope those who work on the Kprize feel.

One day in early 2024 I had the idea to put them all of the above together and the Kprize was born\! I assembled a team to adapt SWE-bench’s collection pipeline and implement the evaluation part on Kaggle’s infrastructure. For this competition we will collect a new test set after the submission deadline.

Finally, shoutouts to the core members of the Kprize team for standing this up: Chris Rytting, Justin Field, Alex Shaw, and K. Tighe. And also thanks to Kaggle for their deep partnership.

Happy hacking\!

Check out [my NeurIPS announcement slides](https://docs.google.com/presentation/d/1yp8xWBLB9Uf6VwDFk6SznreUUsegK78jHBAVCuVPAVw/edit?usp=sharing)