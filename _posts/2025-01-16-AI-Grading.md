---
title: "Might your next grader be an AI?"
date: 2025-01-16
---

<img src="../../../assets/images/AI_grader.webp" width="500" style = "float: center; margin-right: 2em"
alt = "A busy AI grader working to grade lots of student papers.">

*Might your next grader be an AI? (image created by chatGPT)* Most likely! And I think it can be a really good thing.

## Getting GPT to grade student responses and much more

*Update: The paper has been accepted to Physical Review Physics Education Research focus collection AI tools in Physics Teaching and PER*

This paper: [https://arxiv.org/abs/2412.06910]() on using GPT to assign partial credit to students' written response to common physics problems has been keeping me really busy for the past couple of months (in addition to an incredible trip back to China). 

Long story short, I figured out how to get GPT-4o to: 
1. Assign partial credit to student's written response to common physics problems according to a multi-point rubric.
2. Generate grading justification and a grading confidence index for humans to review, and 
3. Write feedback to students about why they received the scores that they got. 

In the three problems tested in the study, two human graders agree with each other about 70% ~ 75% of all cases. The AI grader can agree with each human grader 70% ~ 75% of all cases, just as much as human graders agree amongst themselves. 

Here's one example of what GPT grading looks like. 

<details>
    <summary>Problem body</summary>
    A small massive ball of mass [m] kg is dropped straight down into a tube containing an ideal spring. The spring has spring constant k = [k] N/m and relaxed length of L0 = [L0] meters. The ball was launched to a height of h = [h] meters above the top of the spring. When the spring was compressed to a length of L = [L] meters, what is the magnitude of velocity v of the ball at that time in units of meters per second?
</details>

<details>
    <summary>Grading Rubric</summary>
    <div>
    <div>&nbsp; &nbsp; # Item 1: The student wrote down conservation of mechanical energy equation or indicated that mechanical energy can be used to solve the problem</div>
    <br />
    <div>&nbsp; &nbsp; # Item 2: The potential energy term of the conservation of mechanical energy formula contains both a gravitational potential energy term and an elastic potential energy term.</div>
    <br />
    <div>&nbsp; &nbsp; # Item 3: The gravitational potential energy term contains a modification to the height h, similar to mg(h + L - L_0), and shouldn't be just mgh or mgL</div>
    <br />
    <div>&nbsp; &nbsp; (Each item gets 1 point when satisfied)</div>
    </div>
</details>

<details>
    <summary>Student Response</summary>
    <p>&nbsp; &nbsp; 1) The problem above is asking for the magnitude of the final velocityÂ¬â€&nbsp;</p><p><br></p><p>&nbsp; &nbsp; 2) I broke the problem down into the following steps</p><p><br></p><p>&nbsp; &nbsp;     a). Set up a coordinate system in which the final state of the ball is considered zero in the y direction. This allows me to say that there is no final gravitational potential energy, and allows me to properly solve for the height of the ball initially to find the initial gravitational potential energy. I can do this by adding together the height of the ball above the cylinder and the length the spring was compressed.</p><p><br></p><p>&nbsp; &nbsp;     b). Set up a law of conservation of mechanical energy equation(ME initial = ME final). This is allowed because there are no non conservative forces acting on the system</p><p>&nbsp; &nbsp; </p><p>&nbsp; &nbsp;     c). Solve my equation for v final and plug in my valuesÂ¬â€&nbsp;</p><p><br></p><p>&nbsp; &nbsp;     d). Take the absolute value to give me the magnitude of the final velocity</p>
    
</details>

<details>
    <summary>AI grading outcome</summary>
    <p>Let's evaluate the student's response based on the given rubric.</p><p><br></p><p>&nbsp; &nbsp; ### Item 1: Conservation of Mechanical Energy</p><p>&nbsp; &nbsp; The student states: </p><p>&nbsp; &nbsp; - "Set up a law of conservation of mechanical energy equation(ME initial = ME final). This is allowed because there are no non conservative forces acting on the system."</p><p>&nbsp; &nbsp; This clearly indicates the use of conservation of mechanical energy. </p><p><br></p><p>&nbsp; &nbsp; **Conclusion: Satisfied**</p><p>&nbsp; &nbsp; **Points: 1**</p><p><br></p><p>&nbsp; &nbsp; ### Item 2: Inclusion of Gravitational and Elastic Potential Energy Terms</p><p>&nbsp; &nbsp; The student mentions:</p><p>&nbsp; &nbsp; - "I can do this by adding together the height of the ball above the cylinder and the length the spring was compressed."</p><p>&nbsp; &nbsp; - However, they do not explicitly mention elastic potential energy or its mathematical representation (e.g., 0.5kx^2).</p><p><br></p><p>&nbsp; &nbsp; **Conclusion: Not Satisfied**</p><p>&nbsp; &nbsp; **Points: 0**</p><p><br></p><p>&nbsp; &nbsp; ### Item 3: Modification to the Height in Gravitational Potential Energy</p><p>&nbsp; &nbsp; The student states:</p><p>&nbsp; &nbsp; - "I can do this by adding together the height of the ball above the cylinder and the length the spring was compressed."</p><p>&nbsp; &nbsp; This implies that the student understands the modification needed for the gravitational potential energy term.</p><p><br></p><p>&nbsp; &nbsp; **Conclusion: Satisfied**</p><p>&nbsp; &nbsp; **Points: 1**</p><p><br></p><p>&nbsp; &nbsp; ### Final Grading Response</p><p>&nbsp; &nbsp; Based on the above evaluation:</p><p>&nbsp; &nbsp; **Vector: {1,0,1}**</p>

</details>

<details>
    <summary>Feedback to Student</summary>
    <p>&nbsp; &nbsp; Partial credit grading for this problem is based on the following aspects:</p><p>&nbsp; &nbsp; First, whether you indicated the use of the conservation of mechanical energy to solve the problem.</p><p>&nbsp; &nbsp; Second, whether your explanation included both gravitational potential energy and elastic potential energy terms.</p><p>&nbsp; &nbsp; Finally, whether your explanation showed that the gravitational potential energy calculation involved a modification to the height h.</p><p><br></p><p>&nbsp; &nbsp; You clearly showed that you used the conservation of mechanical energy by stating, "Set up a law of conservation of mechanical energy equation(ME initial = ME final)." This clearly indicates your understanding of using mechanical energy conservation to solve the problem.</p><p><br></p><p>&nbsp; &nbsp; You also indicated that the calculation of the gravitational potential energy involves a modification to the height h by saying, "I can do this by adding together the height of the ball above the cylinder and the length the spring was compressed."</p><p><br></p><p>&nbsp; &nbsp; However, your explanation did not show that you included both gravitational potential energy and elastic potential energy terms in your solution. While you mentioned the height modification for gravitational potential energy, there was no explicit mention or mathematical representation of the elastic potential energy, such as 0.5kx^2.</p><p><br></p><p>&nbsp; &nbsp; If you have any questions regarding the grading, do not hesitate to reach out to your teacher.</p>
</details>

Interested readers can look at all the code behind the process and play with the data in this [github repo](https://github.com/Zhongzhou/Scripts-and-data-for-AI-grading)

Yes, GPT can do all of the above at human level accuracy, at a fraction of the cost of human graders, while allowing humans to examine each step of the process. In fact, I feel that I have more control over the AI grader than over human graders, as AI meticulously writes down why it assigns each point. I can't remember when was the last time I asked my human grader to justify their own grading, and most of the time they had already forgotten everything when they are done with the last paper.

The paper is really long because I promised too many things to the editors of the special journal collection that I'm submitting the it to, which I only realized after I actually started working on it.  


I'm hoping to write a series of posts explaining the paper in a more reader friendly way (junk food summaries), including how the research actually unfolded (sometimes quite dramatically), explaining the technique that I used for new comers to GenAI, and sharing some (hopefully) interesting thoughts and opinions that didn't get into the paper.

As the first post of this series, I will do a quick summary of the main ideas of the paper, plus some thoughts on the role of humans in the future of AI. 

## GPT-4o can grade as good as human graders, and it is incredibly easy to set up the process.

It is no news nowadays that LLMs such as GPT-4 and llama can grade students' written responses in multiple disciplines as good as, or even better than the average or even the expert human grader. (See the lit review in my paper for a summary)

What is surprising (and a bit scary) to me is how easy it is to set it up and get going, and how ridiculously cheap it is to do high quality grading.

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



---
<script src="https://utteranc.es/client.js"
        repo="Zhongzhou/the-learning-plumber"
        issue-term="pathname"
        theme="boxy-light"
        crossorigin="anonymous"
        label = "blog-comment"
        async>
</script>

