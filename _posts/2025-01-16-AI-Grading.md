---
title: "Your next grader may just be an AI"
date: 2025-01-16
---

This [paper on using GPT for partial credit grading](https://arxiv.org/abs/2412.06910) has been keeping me really busy for the past couple of months (in addition to an incredible trip back to China). The paper is really long because I promised too many things to the editors of the special journal collection that I'm submitting the paper to, which I only realized after I actually started working on it.  

Long story short, I figured out how to get GPT-4o to: 
1. assign partial credit of students' written response to common physics problems according to multi-point rubric
2. generate grading justification a grading confidence index for humans to review, and 
3. write feedback to students about why they received the scores that they got. 

Yes, GPT can do all of those efficiently and consistently, while still allowing humans to have sufficient oversight on the grading process. In fact, I feel that I have more control over machine grader than over human grader, because AI meticulously writes down why it assigns each point. I can't remember when was the last time I asked my human grader to justify their own grading, and most of the time the graders have already forgotten their reasoning after all the grading is done.

I'm hoping to write a series of posts explaining the paper in a more reader friendly way (junk food summaries), including how the research actually unfolded (sometimes quite dramatically), explaining the technique that I used for new comers to GenAI, and sharing some (hopefully) interesting thoughts and opinions that didn't get into the paper.

Interested readers can look at all the code behind the process and play with the data in this github repo: https://github.com/Zhongzhou/Scripts-and-data-for-AI-grading

As the first post, I will do a "junk food" version summary of the main ideas of the paper as usual, plus some thoughts on the role of humans in the future of AI. 

# GPT-4o can grade as good as human graders, and it is a bit scary how easy it is to achieve that

It is no news now that LLMs such as GPT-4 and llama can grade students' written responses as good as, or even better than your average or even expert human grader.What is surprising to me is how easy it is to set it up and get going, and how ridiculously cheap it is to do high quality grading.

In my case, GPT can grade about 100 student written responses on a 3 point rubric, generate confidence intervals, and write individual feedback to every student in about 1 hour, and cost under $5. Yes, you heard me right, 1 hour, $5, and it is getting cheaper and better by the day.

You don't need any "training data" to train the model, just get a GPT-4o subscription, and all it takes to set up the process is the following:

1. *Write some clear instruction to students*, asking them to articular their reasoning process about a problem in words. Pure math derivation is still a challenge for GenAI as far as I know. It can be either conceptual problem or calculation problem. (I didn't try graphs or sketches but others have already tried that)

2. *Write the grading rubric*. Now here is my big discovery: for GPT to grade well, you must carefully explain your criteria for each rubric to it, as if you are explaining it to a very smart grader who has never taken this course before. For example, if the rubric says "students used conservation of mechanical energy to solve the problem", you need to tell GPT that if a student writes something like "1/2mv^2 = mgh", or even "mv^2 = mgh" (with a typo), it counts as yes for that rubric item. How much explanation is needed for best performance can be a bit tricky (as you can see in the paper), but one can do a couple of quick test runs to get it to work. 
I'll explain that part more in a future post. 

3. *Let GPT grade 5+ times*, and take the most common grade. This always gives better performance than grading it once, and the outcome is far more stable. 




