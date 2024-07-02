---
title: "Creating the Learning Plumber image using GPT-4o"
date: 2024-07-01
---

Many people still don't realize how detailed the prompt needs to be for GPT to generate good quality images. 

Here' the prompt I gave GPT-4o for the title image:

    "I would like to generate an image for my new blog named "The learning plumber". The name was inspired by the following reasons:
    """  1. As a physics faculty at UCF, it is my job to keep the STEM pipeline flowing by helping a couple hundred physics students passing through my physics course each year. 
    2. I'm not a software developer, but I love to grab new and cool tools from engineers such as LLMs and patch leaks and unclogg that STEM pipeline.
    3. I have a lovely wife and two lovely daughters....I'm destined to be THE PLUMBER in our house for the rest of my life!!! """

    I want this figure to be a 2-D, cartnoon-ish depiction of a cool, tech savvy plumber working with tools on pipes, but what flows through the pipes are knowledge of math and physics, and students. One of the tools that the plumber is using is generative AI and LLMs. "

This result is this image:

<img src="../assets/images/the-learning-plumber.webp" width="250" 
alt = "an AI generated image of the learning plumber">

This is quite a bit improvement over this older version which I simply told it to "genrate an image for a blog named "the Learning Plumber".".

<img src="../assets/images/the-learning-plumber.png" width="250"
alt = "an AI generated image of the learning plumber">

However, none of the letters/words on this image makes any sense. This is a very obvious drawback of LLM generated images: a mix of image and non-image objects (such as text). Image generator should be couples with text/symbol generators, and I think it would be possible to train an LLM to place text on appropriate locations so that the output best represents the intended visual effect. 

