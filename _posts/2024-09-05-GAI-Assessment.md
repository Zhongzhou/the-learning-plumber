---
title: "Junk Food Summary of a Very Healthy Paper on GenAI and Assessment"
date: 2024-09-05
---
# The Junk Food Summary of a Healthy Paper
Some papers are like a giant bowl of Quinoa salad with no dressing: you know it is really good for you but you just need a lot of self-discipline to finish it.

Here is one such paper: Kaldaras, L., Akaeze, H. O., & Reckase, M. D. (2024). Developing valid assessments in the era of generative artificial intelligence. Frontiers in Education, 9, 1399377. [https://doi.org/10.3389/FEDUC.2024.1399377/BIBTEX]. It has an whole lot of great stuff, but, I have say that reading through it requires a couple cups of coffee to say the least.

So I decided to create a "junk food" version summary of this paper: it will be unhealthy and probably miss a LOT of the intellectual vitamins in the original salad bowl, but, hopefully it tastes better 😄

# The Core Message
Suppose we want to know if someone knows how to make a burger :hamburger:. Traditionally, the tests contain multiple choice questions such as "Which of the following ingredients are included in a burger?". Now, with GenAI, we can ask the person: Tell us, how do you make a burger? and use GenAI to grade it. Nice. But how do we know if those new GenAI based tests really reflect someone's ability to make a juicy burger? That is the question of test validity.

## The future of tests
What should test in the future be like? The authors listed three things:
1. Emphasize and real-world application rather than memorization.
2. Able to assess learning as a process
3. Able to provide meaningful feedback for growth.

In other words:
Do you know how to make a burger? Don't just memorize the recipe or the ingredients. Between burger newbie and burger master, which stage are you at? Do you need to practice flipping the pattie, or learn more about different types of cheese?

So how can we build those future tests? And how can GAI make creating those tests much more feasible?

# Behind every test there should be a construct. Wait, a what?
*"A construct refers to an unobservable and possibly hypothetical entity or concept."* that the test is supposed to measure. 
Personally, I think that this definition has an important implication: if an entity/concept is unobservable and hypothetical, then it is "constructed" by humans through language and social consensus, rather than an objective existence. I also think that "unobservable" should be "not directly observable", since a completely unobservable entity sound like the famous "invisible dragon in my garage". 

The more I think about the definition of a "construct", the less I think I understand it. Below is a "junk food" version of how I currently understand this concept, which is highly debatable but hopefully has some truth to it:

Whether a sandwich is a hamburger, a cheeseburger, or a bacon burger, is an objective existence that is not hypothetical, nor purely constructed (one can always question what counts as a piece of cheese, for example, but in most cases it is obvious.)

"How would you like your burger cooked", refers to a "constructed" concept. Terms such as "medium rare" are constructed by humans, and no two restaurants can 100% agree on how rare is "medium rare". But this is still not a "construct", since the "cookedness" of a beef pattie is directly observable (or tastable) if you cut it open or bite into it.

"How good is the guy making the burger" is likely a construct. Yes, you can observe the person cooking a burger, but "goodness" of burger cooking at some point would involve brain states such as knowledge related to burger and cooking, physical aptness such as hand-eye-coordination, etc. You can't cut-open someone's brain, and even if you sort of can (for example, using fMRI), you won't be able to directly see a "burger making" area as assess its goodness. You are also assuming that the "goodness" of burger cooking can be mapped onto a one dimensional scale from "terrible" to "master". All of those are hypothetical, and needs to be validated. 

"How creative is this person when it comes to making burgers" is totally a construct because 1. you can't observe creativity directly, and 2. I just made the **** up. 

In fact, after writing this all down, I think we either need a much better definition of "construct", or give up on the idea of a "construct" altogether.

## The construct validity: is a good burger really good?

*"Construct validity relates to how well an assessment instrument represents and reflects the construct of interest.The validation process involves accumulating multiple relevant evidence sources to provide sound scientific support for the proposed interpretation of the assessment results"*

Say we have some kind of a test of how good a burger is, without actually tasting it. The "construct" here is the goodness of a burger, and testing the "construct" validity is relatively straightforward (just relatively). Give some burgers to a large group of people and ask them to rank it. Then compare the ranking to the test results, and you have the construct validity of the test. In addition, examining how uniform people rates those burgers will give you a validity measure of the construct itself, which may also be called construct validity I guess?

Now validating a real "construct" is much more difficult, since it cannot be directly observed, nor can we easily define some ground-truth, such as the taste of a burger. So, multiple sources of evidences needs to be collected to validate that the test is actually testing the "construct" we are interested in.

## How you use the test score matters!!
*"Consequently, when assessment results are interpreted in multiple ways—for example, as a summative measure of what students have mastered or as a predictive measure of future performance—each of these intended uses of the assessment result must have evidence to support the desired inference."*

This is an extremely important point in my opinion, and is all too often completely left to the side. Say we have a valid test of how good tasting a burger is, yay! Now let us use that to decide which worker wins the "best burger maker" award based on how good their burger is! Sounds fair? What about a burger maker who works at McDonalds vs. a burger maker who works at a 4-star hotel restaurant? That's obviously not fair.

But what about "you need to get a C+ average to receive scholarship"? Or "C+ in Calculus I" to be able to take physics I? We don't even think about those questions, let alone doing something about it. Oh, and student rating > 3.0 to be eligible for teaching award, let's not even go there....

**When a test result is used for a purpose, there needs to be evidence of that particular use**

## Construct proficiency levels: How would you like your eggs cooked??

The egg is an amazingly precise thermometer. As the temperature rises, it goes from raw egg to runny yolk, to soft boiled to hard boiled, following a precise, well defined sequence. The white solidifies faster than the yolk, making runny yolk egg a reality. We know that process extremely well (Harvard Science of Cooking uses it as an example!), simply because we can crack open the egg and look inside at any point. 

How many stages are there when a student transitions from novice to expert? Unfortunately, cracking students' head open and peak inside is and will never be an option (although perhaps every teacher had thought about it at some point). So "construct proficiency level" becomes really hard to measure, especially since in hypothetical "construct" itself may not even be a good hypothetical model of the brain.

Generative AI(GAI) provides a way to look into the mind and find those transition patterns, argues the paper. For example, one could ask students to write their response to a question, and use LLMs to find patterns and clusters in student answers, through for example text embedding and clustering process. One could either give the same or similar problem repeatedly to a small group of students and observe the transition of answers, or to a large enough student population, assuming that there must be students with different levels of proficiency of the construct, or both. This process uses LLM's ability to detect similarity in language, and that language serves as the best representation of the mind (see [this post](./2024-08-23-Language-Thought.md)) that humans have. Clearly, using GAI to do this will be much easier and more streamlined compared to having humans code hundreds of student responses.

# Five sources of evidences of construct validity

Evidence sources outlined in the Standards for Educational and Psychological Testing include: 
1. Evidence based on test content; 
2. Evidence based on response process; 
3. evidence based on internal structure; 
4. evidence based on relation to other variables; 
5. validity generalization.

Yes, it is much harder than the hardest boiled egg.

## Evidence based on test content: is it really about the burger?
*"This type of evidence relates to analyzing the relationship between the test content and the construct it is intended to measure."*

A burger test should be about burgers, so the question "how do you use fork and knife to eat food" has no content validity, unless the correct answer is "you don't". 

A physics test should be about physics. Yet, I was going through all the back of chapter problems of a popular textbook recently and was struck in the head by a baseball problem. That problem is clearly assessing students' baseball terminology and familiarity with the baseball court!

(To be continued)

---
<script src="https://utteranc.es/client.js"
        repo="Zhongzhou/the-learning-plumber"
        issue-term="pathname"
        theme="boxy-light"
        crossorigin="anonymous"
        label = "blog-comment"
        async>
</script>