---
title: "Can LLMs actually understand anything? Sharing interesting papers about language and cognition (2)"
date: 2024-08-24
---

# Can LLMs Understand the World? Maybe?

**No, they cannot**, argue the authors of this paper:
[Dissociating language and thought in large language models](https://www.sciencedirect.com/science/article/abs/pii/S1364661324000275)

Not surprising given that the last author on this one is the first author on the Nature paper claiming that language is separated from thought. LLMs are computer systems trained to learn language, the code system that humans use to generate thought. So they can, and have, learned the functions of the "language network" extremely well, arguably much better than any human. However, these systems cannot figure out the actual cognitive process behind the code, just from studying and mimicking the code itself. That's because the cognitive process is carried out by separate and different systems in the brain, which the neural networks of LLMs are not designed to mimic. For example, lots of cognition involves the visual domain or the sensory motors (remember [Grounded Cognition](http://www.ncbi.nlm.nih.gov/pubmed/17705682)?), and LLMs themselves have neither. (At least LLMs alone don't have those domains.) 

**Right?**

I came across some really surprising studies of language models seem to suggest otherwise:
[LLMs develop their own understanding of reality as their language abilities improve](https://news.mit.edu/2024/llms-develop-own-understanding-of-reality-as-language-abilities-improve-0814)

[Large Language Model: world models or surface statistics?](https://thegradient.pub/othello/)

[Actually, Othello-GPT Has A Linear Emergent World Representation — Neel Nanda](https://www.neelnanda.io/mechanistic-interpretability/othello)

Simply put, people trained language models on learning written solutions of puzzles or games, such as board recordings of Othello. The LLMs never saw the board, not have the neural nets to process visual input, just learned to predict the next line of board recording based on all the previous recordings. So, it shouldn't be able to understand the spatial structure of the board, right?

Well, when people probed inside the neural nets (I have to say that the details are very much beyond me), they found evidences that deep inside the neural nets of LLMs, there are structures that probably represented the spatial structure of the Othello board, or the puzzles given to the LLMs. In other words, the neural nets somehow "figured out" that all the records have some basic logic behind them (for example, the Othello board).

**So they can understand us after all?**

Not exactly. The above studies trained LLMs on extensive amounts of records, all focused on a fairly simple, and very well defined system (a game or a puzzle). There's very limited amount of "language rules" to figure out, so the neural nets ended up figuring out the spatial relations behind the language rules, which is more efficient for prediction. Very rarely do we ever encounter such as case where the underlying relation is well defined and limited, while at the same time there are near infinite amounts of code that is clearly labeled and dedicated to the system. 

In the case of learning from the internet, the world behind the code is exponentially more complicated, ill-defined, and fuzzy. The language representation of it, on the other hand, is sparse (relative to the world they were representing) and extremely noisy. In that case, prediction is much more accurate if one just tries to "mimic the language", compared to trying to figure out the actual laws of the world (and humans!).

For me, the situation is somewhat very loosely analogs to students learning science:

If you have a giant problem bank to practice from, and a very well written textbook, and your task is just to figure out how to do two digit addition, you are definitely going to learn two digit addition!

On the other hand, if you are trying to learn Quantum Mechanics from just listening to your teacher, who speaks with a thick Chinese accent, and your exam is whether you can give a talk on Quantum Mechanics to a group of general audience, you are going to learn next to nothing about Quantum but do a very good job talking Chinglish!

(I realized that this is just another version of the [professor and driver joke](https://www.reddit.com/r/Jokes/comments/69xteu/the_professor_and_his_driver/) while writing this piece, another case of language facilitated cognition!)

## What does all this have to do with teaching and learning?

Now this piece is really turning in to a trilogy....I'll write about that part next week!

---
<script src="https://utteranc.es/client.js"
        repo="Zhongzhou/the-learning-plumber"
        issue-term="pathname"
        theme="boxy-light"
        crossorigin="anonymous"
        label = "blog-comment"
        async>
</script>