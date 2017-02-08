---
title: "Code Review Best Practices"
teaching: 5
exercises: 0
questions:
- "What are some best practices for code reviews"
objectives:
- "Learn about effective practices for code reviews."
keypoints:
---
A successful strategy for code reviews requires balance between strictly documented processes and a 
non-threatening, collaborative environment. Highly regimented reviews can stifle productivity, yet 
lackadaisical processes are often ineffective. Establising a middle 
ground where the review can be efficient and effective while fostering open communication and 
knowledge-sharing is essential.

## For Everyone

### Review the right things, let tools to do the rest

You don’t need to argue over code style and formatting issues. There are plenty of tools which can 
consistently highlight those things. Ensuring that the code is correct, understandable and maintainable 
is what’s important. Sure, style and formatting form part of that, but you should let the tool be the one 
to point out those things.

### Everyone should code review

Some people are better at it than others. The more experienced may well spot more bugs, and that’s 
important. But more important is maintaining a positive attitude to code review in general and that 
means avoiding any ‘Us vs. Them’ attitude, or making reviewing code burdensome for someone.

### Review all code

No code is too short or too simple. If you review everything then nothing gets missed. What’s more, 
it makes it part of the process, a habit and not an after thought.

### Adopt a positive attitude

This is just as important for reviewers as well as submitters. Code reviews are not the time to get 
all alpha and exert your coding prowess. Nor do you need to get defensive. Go in to it with a positive 
attitude of constructive criticism and you can build trust around the process.

## For Reviewers

### Code review often and for short sessions

The effectiveness of your reviews decreases after around an hour. So putting off reviews and doing 
them in one almighty session doesn’t help anybody. Set aside time throughout your day to coincide 
with breaks, so as not to disrupt your own flow and help form a habit. Your colleagues will thank 
you for it. Waiting can be frustrating and they can resolve issues quicker whilst the code is still 
fresh in their heads.

### Take your time

![]({{ site.github.url }}/fig/code-review-best-practices-figure-02.gif)

Code reviews in reasonable quantity, at a slower pace for a limited amount of time result in the 
most effective outcomes.

### It’s OK to say “It’s all good”

Don’t get picky, you don’t have to find an issue in every review.

### Use a [checklist]({{ page.root }}/02-checklist

Code review checklists ensure consistency – they make sure everyone is covering what’s important and common mistakes.

## For Submitters

### Keep the code short

![]({{ site.github.url }}/fig/code-review-best-practices-figure-01.gif)

Beyond 200 lines and the effectiveness of a review drops significantly. By the time you’re at more than 
400 they become almost pointless.

### Provide context

Link to any related tickets, or the specification, using code review tools if necessary. 
Provide short, but useful commit messages and plenty of comments throughout your code. It’ll help the 
reviewer and you’ll get fewer issues coming back.