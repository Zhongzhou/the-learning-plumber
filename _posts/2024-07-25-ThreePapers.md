---
title: "Quirky Summary of Three Recent Papers on GenAI"
date: 2024-07-25
---

## Paper 1: Students actually like AI generated Feedback!

A very early and primitive attempt at prompt engineering GPT-3.5 to generate feedback for students on conceptual physics questions. Turns out, students actually like AI Generative feedback (if you don't tell them its AI). The reason might be that when faced with 100 student responses to grade, any human instructor will lose patience after the first 20, but AI just keeps writing....

[Exploring generative AI assisted feedback writing for students’ written responses to a physics conceptual question with prompt engineering and few-shot learning](https://journals.aps.org/prper/abstract/10.1103/PhysRevPhysEducRes.20.010152)

## Paper 2: AI can grade! (but you need to tell it how and force it to think)

Did some interesting prompt engineering attempts at making gpt-3.5 grade student answers for a physics question. The key to high performance? Tell it what counts and doesn't count as a correct answer for each rubric, just like you teach your newbie TA!. 

Also, GPT seems to be quite "lazy". If you don't force it to think, it will just make a guess. If you don't force it to think before giving the grade, it will just guess a grade and then make up some reasoning. Totally appropriate for a 3-year-old, right? (don't quote me on that)

[Achieving Human Level Partial Credit Grading of Written Responses to Physics Conceptual Question using GPT-3.5 with Only Prompt Engineering](https://arxiv.org/abs/2407.15251)


## Paper 3: What should we do when we can have LOTs of test problems?

This one has the least to do with AI, but I personally like it the most. It is the first step towards answering this question: Now that we can easily create lots of isomorphic problems using AI, what can we do with all those problems? In this paper we try to see if we can give students lots of attempts on quizzes, each time with a slightly different set of problems, and see if students learn from all those attempts. Or did all those extra attempts make the quiz too easy for those who didn't understand it that well? The answer: it depends. (yeah, yeah.....)

I like it the most because: Florida gets hit by 1+ hurricane every fall semester, and every time when I have to process excuse notes to reschedule an exam I was like, urghhhhhh....., and so are my student!
I also like it because this is the type of research that instead of asking *how can we use AI to do what we do*, it asks *how can we use AI to do things that we've never done before?*

[Comparing student performance on a multi-attempt asynchronous assessment to a single-attempt synchronous assessment in introductory level physics](https://arxiv.org/abs/2407.15257)

---

<script src="https://utteranc.es/client.js"
        repo="Zhongzhou/the-learning-plumber"
        issue-term="pathname"
        theme="boxy-light"
        crossorigin="anonymous"
        label = "blog-comment"
        async>
</script>