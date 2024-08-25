---
title: "Can LLMs actually understand anything? Sharing interesting papers about language and cognition (1)"
date: 2024-08-23
---

The one benefit of doing a sabbatical is that I actually have time to sit down in a Starbucks and read papers. Like really read in a way that is actually enjoyable and thought provoking. I've been reading some really interesting papers which I would love to share. (Also see my next post on [LLM and understanding](./2024-08-24-LLM-Understanding.md))

# Language is not Cognition: wait, waht? what me saying? You get it.

In this paper: [Language is primarily a tool for communication rather than thought](https://doi.org/10.1038/s41586-024-07522-w), the authors claim that:

Language is not necessary for *ANY* type of cognition (other than comprehending language itself, of course). Cognitive functions such as logical reasoning are carried out in areas of the brain that is separate from (albeit adjacent to) the "language network" in the human brain. (Yes, language is processed via a network of connected areas in the brain, not just the famous Broca’s and Wernicke’s areas)

Really? Nothing? None? That was my first reaction but then I realized how much difficulty I always had organizing my thoughts into proper words, and the idea seem much more believable.(the section title is an example of this and contains an intentional spelling error.)

The paper cites decades of research, especially neuro-imagine research to back this claim. Most of those are not too surprising, for example, language is not involved in math or logical reasoning. Larry Barsalou's [Grounded cognition](http://www.ncbi.nlm.nih.gov/pubmed/17705682) theory predicted that back in the early 2000. What is very surprising to me is that even computer code comprehension doesn't require the language area either!! 

(Well, the paper they cited actually says that the language network is indeed active when reading Python, but much weaker compared to reading real language. See here [Comprehension of computer code relies primarily on domain-general executive brain regions](https://doi.org/10.7554/eLife.58906). Visual domain is actually much more important in understanding code logic. Grounded Cognition again!)

Ok, I am pretty much convinced that thinking can be, and probably is in most cases, done without language (otherwise writing would be much easier!). Language in our mind is probably a by-product of our thoughts. But I still have one more question:

Can language help us think better?

My question came from both education research and observation from teaching. Any experienced teacher who has ever done office hour will be familiar with the following situation:

A student comes into office hour, completely confused, often frustrated or even angry, and claims that they have no idea how to solve a problem. An experienced teacher, instead of jumping immediately into helping the student, will ask this question:

*"Tell me, how did you try to solve this problem?"*

Once the student started talking, oftentimes, after a while the student will go "oh, wait a minute....hold on....." and then they often talks themselves out of the problem. The best part is that they always thank the teacher helping them!

## Might language be the facilitator of complex cognition? My little thought experiment
Here is a totally un-scientific personal experiment in by brain: If I consciously control myself to not "speak" within my brain while thinking, I am able to come up with ideas just fine, but I feel that I have a lot of difficulty going from one idea to the next. It is as if I don't have an efficient way of compressing and storing my thoughts in working memory, so my brain gets stuck in one place.

So, could language, or more precisely, self-conversation (partial activation of the language network), be a useful tool for thought regulation? 

One hypothesis is that if thoughts (or ideas) are distributed activation of neural networks across the brain (borrowing a page again from Barsalou's Perceptual Symbols System), then our brain could utilize that language network to increase the weights of some parts of that distributed activation and suppress other parts. By doing that the brain frees up cognitive capacity to move on to new thoughts. It might also utilize language as a "compression" tool for thoughts, and store compressed thoughts as language in long term memory.

After-all, from an evolution perspective, it is unlikely that human brain would evolve a dedicated language network that is located in close proximity to other cognitive domains, yet never try to use it to boost cognition. Might it also be possible that parts of language network originated from brain areas previously used for regulation of cognition?

## My (totally made up) hypothesis of the mechanism by which language regulates cognition

I quickly came up with the following hypothesized mechanism for language as a regulator for cognition while in Starbucks reading those papers:

Given that we know the human brain performs the following actions during communication:

* From cognition produce language as output (speak)

* From language as input perform cognition (listen and understand).

It almost seem inevitable to me that the brain is capable of treating its own output of language as input (because you always hear your own speaking and presumably your brain doesn't shut down to your own words). This of course will lead to significantly less activation in the language areas, but non-the-less some activation (just like in the python code comprehension task). Therefore, what might happen in the brain during self-conversation is this:

*Cognition -> (internal) language -> Cognition.*

If language were a perfect and lossless representation of cognition, then this process produces nothing new (a dead loop). However, we know very well that it is not (otherwise there won't be any misunderstanding, what a wonderful world!). Therefore, what most likely happens in the brain is this:

*Cognition -> (internal) language -> Somewhat different Cognition.*

The somewhat different cognition is generated by the brain interpreting its own language, and thereby adjusting the conscious attentional focus to different parts of the current cognition, which would otherwise remain in sub-conscious. 
This loop process can go on and on to continuously produce new ideas, using self-conversation as both a regulation and a compression tool.

Of course, the brain can also directly do this:

Cognition -> New and different Cognition.

But those two processes can be very different, and my hunch is that the process with language as intermediate may have an advantage over the direct cognition to cognition rout. One possible reason is that it expands working memory by compressing the previous cognition, and storing it via the help of the language network.

This hypothesis might be difficulty to test as one would need to somehow shut down the language network in the brain without interfering with other cognitive functions.

# Can Language Models Understand The World? And what this means for education?

Those are the natural next questions to think about, but this post is already getting too long, so I'm going to write about them in my next post. 

---
<script src="https://utteranc.es/client.js"
        repo="Zhongzhou/the-learning-plumber"
        issue-term="pathname"
        theme="boxy-light"
        crossorigin="anonymous"
        label = "blog-comment"
        async>
</script>