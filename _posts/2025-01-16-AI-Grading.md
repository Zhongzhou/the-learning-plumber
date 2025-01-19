---
title: "Might your next grader be an AI?"
date: 2025-01-16
---

# Might your next grader be an AI? 
## Getting GPT to grade student responses and much more
This [paper on using GPT for partial credit grading](https://arxiv.org/abs/2412.06910) has been keeping me really busy for the past couple of months (in addition to an incredible trip back to China). The paper is really long because I promised too many things to the editors of the special journal collection that I'm submitting the it to, which I only realized after I actually started working on it.  

Long story short, I figured out how to get GPT-4o to: 
1. Assign partial credit of students' written response to common physics problems according to a multi-point rubric
2. Generate grading justification and a grading confidence index for humans to review, and 
3. Write feedback to students about why they received the scores that they got. 

Here's one example of what GPT grading looks like.

<details>
    <summary>Problem body</summary>
</details>

<details>
    <summary>Student Response</summary>
</details>

<details>
    <summary>AI grading</summary>
</details>

<details>
    <summary>Feedback to Student</summary>
</details>


Yes, GPT can do all of those at once, while allowing humans to have extensive oversight on the grading process. In fact, I feel that I have more control over the AI grader than over human graders, as AI meticulously writes down why it assigns each point. I can't remember when was the last time I asked my human grader to justify their own grading, and most of the time they had already forgotten everything when they are done with the last paper.

I'm hoping to write a series of posts explaining the paper in a more reader friendly way (junk food summaries), including how the research actually unfolded (sometimes quite dramatically), explaining the technique that I used for new comers to GenAI, and sharing some (hopefully) interesting thoughts and opinions that didn't get into the paper.

Interested readers can look at all the code behind the process and play with the data in this github repo: https://github.com/Zhongzhou/Scripts-and-data-for-AI-grading

As the first post, I will do a "junk food" version summary of the main ideas of the paper as usual, plus some thoughts on the role of humans in the future of AI. 

## GPT-4o can grade as good as human graders, and it is incredibly easy to set up the process.

It is no news nowadays that LLMs such as GPT-4 and llama can grade students' written responses in multiple disciplines as good as, or even better than the average or even the expert human grader. (See the lit review in my paper for a summary) What is surprising (and a bit scary) to me is how easy it is to set it up and get going, and how ridiculously cheap it is to do high quality grading.

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

Yes. I think so, and it is mostly not because it is cheap, but because it provides near complete transparency in during the grading process.

Yes, AI graders can still make all kinds of grading mistakes, it can be biased against certain types of language for forms of answering, it can overlook very creative and non-conventional answers, it will still make spontaneous mistakes despite our best effort due to the nature of generative AI. Yet a human grader could make ALL of those mistakes too, and in the vast majority of cases we have very little idea how frequently those grading errors are  happen on a daily basis. I mean, how can you ask any grader to write down their justification for every point assigned to every student, when you've just assigned to grade 100 student responses?

To me the greatest strength of an AI grader is that the *entire grading process is extremely transparent, which makes it possible to continuously evaluate and improve its grading quality.*

In other words, even though an AI grader is far from perfect, we can be confident that we can detect those imperfectness, and the next round of grading will always be more fair, more inclusive and more accurate. 

It maybe true that if you put in the same amount of work training a human grader, that grader can surpass the AI grader in a shorter amount of time. But a human grader will leave in a couple of years, but the AI grader will live in the cloud effectively forever.

## Will human graders (or human teachers) become obsolete?

Yes and No, and it is quite a weak Yes versus a very strong **No**. 

* The unlikely "yes": if we stop innovating in teaching and learning, and teach/test exactly the same way as we do today.  Because of all the reasons above, I see no reason why we need human graders to grade student response to the same problems year after year, with no control nor improvement in grading quality and feedback experience. 

* The much more likely "no": 
  * At the very least, we can greatly increase the number of written response questions in the course, as they are so much better for learning than multiple-choice questions. Instead of assigning humans as graders, future teaching assistants will be tasked with creating and evaluating new problems, designing grading rubrics, writing rubric explanations, check for AI grading errors, and improve the prompt design. As I argue in the paper, all of which are essential for the grading process to work and must be done by a human expert, at least in the short term. 

  * More importantly, now more than ever is the time to innovate and rethink the basic building blocks of the entire process of teaching and learning. 
    * What new types of questions or tasks shall we challenge our students? (especially since AI can already solve most conventional tasks) 
    * How can we collect evidences from students' work, and make meaningful evaluation of their knowledge and ability? 
    * How can we enable and empower each individual student to develop according to their own pace? 
    * How do we teach and assess creativity and critical thinking?
    * How can we help students feel motivated and welcomed to learn, and develop their ability regulate their own learning?

  The current generation of GenAI is great at completing tasks that have well established patterns or procedures, such as grading answers to common physics problems. Yet for things that have never been done before, humans need to first experiment, evaluate and establish acceptable and beneficial practices, before AI can replicate the process in a satisfactory and meaningful way. **In other words, AI can help us achieve what we want, but it can never tell us what we want.** The task for human teachers or teaching assistance in the future will be to observe what students need, innovate on how to facilitate and empower students, implement the new methods and strategies (hopefully with the help of AI), and most importantly, examine and evaluate if the new process is actually helping students. After all, AI may replace our brain, but I don't see how it can replace our heart.





