---
title: "Might your next grader be an AI?"
date: 2025-01-16
---

# Might your next grader be an AI? 
## Getting AI to grade student responses and much more
This [paper on using GPT for partial credit grading](https://arxiv.org/abs/2412.06910) has been keeping me really busy for the past couple of months (in addition to an incredible trip back to China). The paper is really long because I promised too many things to the editors of the special journal collection that I'm submitting the paper to, which I only realized after I actually started working on it.  

Long story short, I figured out how to get GPT-4o to: 
1. Assign partial credit of students' written response to common physics problems according to multi-point rubric
2. Generate grading justification a grading confidence index for humans to review, and 
3. Write feedback to students about why they received the scores that they got. 

Yes, GPT can do all of those efficiently and consistently, while still allowing humans to have sufficient oversight on the grading process. In fact, I feel that I have more control over machine grader than over human grader, because AI meticulously writes down why it assigns each point. I can't remember when was the last time I asked my human grader to justify their own grading, and most of the time the graders have already forgotten their reasoning after all the grading is done.

I'm hoping to write a series of posts explaining the paper in a more reader friendly way (junk food summaries), including how the research actually unfolded (sometimes quite dramatically), explaining the technique that I used for new comers to GenAI, and sharing some (hopefully) interesting thoughts and opinions that didn't get into the paper.

Interested readers can look at all the code behind the process and play with the data in this github repo: https://github.com/Zhongzhou/Scripts-and-data-for-AI-grading

As the first post, I will do a "junk food" version summary of the main ideas of the paper as usual, plus some thoughts on the role of humans in the future of AI. 

## GPT-4o can grade as good as human graders, and it is incredibly easy to set up the process.

It is no news now that LLMs such as GPT-4 and llama can grade students' written responses as good as, or even better than your average or even expert human grader. (See the lit review in my paper for a summary) What is surprising to me is how easy it is to set it up and get going, and how ridiculously cheap it is to do high quality grading.

In my case, GPT can grade about 100 student written responses on a 3 point rubric, generate confidence intervals, and write individual feedback to every student in about 1 hour, and cost under $5. Yes, you heard me right, 1 hour, $5, and it is getting cheaper and better by the day. 

You don't need any "training data" to train the model, just get a GPT-4o subscription, and all it takes to get the process up and running is the following:

1. *Write some clear instruction to students*, asking them to articular their reasoning process about a problem in words. Pure math derivation is currently still a challenge for GenAI to understand. 

2. *Explain the grading rubric to the AI*. Now here is my main discovery: for GPT to grade well, you must carefully explain your criteria for each rubric to it, as if you are explaining it to a very smart grader who has never taken this course before. For example, if the rubric says "students used conservation of mechanical energy to solve the problem", you need to tell GPT that if a student writes something like "1/2mv^2 = mgh", or even "mv^2 = mgh" (with a typo), it counts as yes for that rubric item. How much explanation is needed for best performance can be a bit tricky (as you can see in the paper), but one can do a couple of quick test runs to get it to work. 
I'll explain that part more in a future post. 

3. *Ask GPT to state its reason behind the grading*: Ask GPT to not just produce a numerical grading outcome, such as {1,1,0}, but to write down why it decides to grade that way. GPT thinks by the words it created, so asking it to write is essentially asking it to think about the grading. No need to give GPT any example or the correct answer. In fact, given it a standard answer will likely make it perform worse.

3. *Let GPT grade 5+ times*, and take the most common grading outcome among the 5+ grades. This always gives better performance than grading it once, and the outcome is more stable than just a single grading run. Moreover, GPT tends to produce different grading outcomes when it is not so sure about how to grade, so the level of consistency between the 5 or more grading outcomes serve as an indicator of the AI's confidence.

4. *Ask it to write the feedback*. Send GPT the grading outcome, the grading justification, and the student response, and ask it to write the feedback for student based on those info. This step is actually very easy for AI.


As you can see, any instructor with a little bit of python experience and a GPT subscription can setup the process in a matter of days. With the right level of rubric explanation, the AI grader will agree with human graders as much as ,or even more than, any two human graders will agree between themselves. 

## Should our next grader be an AI?

Yes. I think so. But it is not because it is cheap. 

To me the greatest advantage of an AI grader is that the entire grading process is extremely transparent, and can be continuously evaluated and improved. 

Yes, AI can still make all kinds of grading mistakes, it can be biased against certain types of language use, it can overlook very creative and non-conventional answers, it will still make spontaneous mistakes despite our best effort due to the nature of generative AI.

Yet a human grader might fall for ALL of those things too, and in the vast majority of cases we have very little idea about how frequently those grading errors happen on a daily basis. I mean, how can you ask any grader to write down their justification for every point assigned to every student, when they are assigned to grade 100 student responses? But AI does that by default. An AI grader's decision making process can be made almost completely transparent to both the instructor and the student.  

Moreover, whenever we found that AI is making a certain type of mistake, we can always tweak the prompt to make it better next time it grades the same problem. No TA training program can get close to that with human TAs. When your most senior and experienced grader leaves the position, you are basically starting from scratch training new graders. AI grader, on the other hand, will continue to improve as long as the prompt is stored somewhere in the cloud. 

In short, the greatest advantage of an AI grader is that even though it may be far from perfect, it can always be made better the next time. (BTW it is also much much cheaper and faster)

## Will human graders become obsolete?

Yes and No, and it is a weak Yes vs. a very strong No. 

The only situation I can think of where human graders will become obsolete is that if we stop any educational innovation, and teach exactly the same way as we do today. In that case, yes, graders will become completely obsolete, as the will never be able to compete with AI graders. 

Yet this is highly unlikely, since there are so many things that we can do differently and better with AI graders. 

At the very least, we can greatly increase the number of written response questions in the course, as they are so much better for learning than multiple-choice ones. Instead of assigning graders to grade, future graders will be tasked with designing grading rubrics, writing explanations, and checking for AI grading errors. 





