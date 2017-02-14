---
title: "Code Review Best Practices"
teaching: 5
exercises: 0
questions:
- "What are some best practices for code reviews?
objectives:
- "Learn about effective practices for code reviews."
- "Learn what makes reviews work better and what can cause problems."
- "Learn what to look for when conducting a review."
- "Learn what to do when your code is being reviewed."
keypoints:
- "An code review strategy is essential for effective reviews"
- "Don't try to review too much code"
- "A timely approach is better than rushing"
- "Reviews are meant to be constructive"
- "Make sure everyong is familiar and agrees on the ground rules"
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

First of all, you have to understand the change you’re reviewing. If you don’t understand the change, you can’t positively review the change. 
A good commit message should contain the purpose of the change, and if necessary, how that change is being achieved. If, after reading the commit 
messages, you don’t understand what is going on, you should ask for the commit message to be improved.

When you understand the change, there are a few key levels of code review:

* syntax – Is the code well formatted, meeting indentation and whitespace standards and free from parse errors?
* style – Is the code idiomatic for the language, are common error-prone patterns for that language avoided, is the code easily understood?
* functional – Does the code do what it’s supposed to do?
* architecture – Is the code required, are there any improvements to be made through abstractions, reuse of other code. Does the code tie in with the 
rest of the codebase?

The first two of these are excellent candidates for automated checks – particularly as from a reviewer’s point of view, 
they’re really tedious to review, and from a reviewee’s point of view, they can feel like nitpicking. If the code 
has to meet such automated checks before it even gets to review, then the human element can be saved for the deep 
structural thought.

Comment on specific lines of code if you can to say where the code doesn’t meet standards or could be improved. 
General feedback on the change as a whole can typically be provided as a comment without referencing a specific line.

Assume best intentions, and try and address the code rather than the person writing the code. Criticism should never be personal.

Code reviews should be objective where possible. There are always subjective preferences in any code base, 
but such preferences should be decided at a team level beforehand, and then be well documented – by pointing 
to such documentation in the code review, the feeling of subjectivity can be avoided. As you come across 
undocumented preferences, determine that they are what the team wish to use, and document them.

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

### Use a [checklist]({{ page.root }}/02-checklist)

Code review checklists ensure consistency – they make sure everyone is covering what’s important and common mistakes.

## For Submitters

### Adhere to the standards of your code base

Most teams agree on standards such as code formatting and style. Make sure your changes adhere to these standards, using an
automated tool - if available. This will avoid wasting time in the review identifying formatting problems.

### Assume best intentions from the reviewer

Realise that a code review is not a battle, and try not to take criticism of your code personally. However, if criticism is personal, then you should say so.

Try and reduce conflict resulting from misunderstandings – see if you can clear up such misunderstandings, either in the review, in the commit messages or through talking it through with the reviewer.

### Keep the code short

![]({{ site.github.url }}/fig/code-review-best-practices-figure-01.gif)

Beyond 200 lines and the effectiveness of a review drops significantly. By the time you’re at more than 
400 they become almost pointless.

### Provide context

Ensure that your commit messages explain what you are trying to achieve and why. Link to any related tickets, or the specification, 
using code review tools if necessary. Provide short, but useful commit messages and plenty of comments throughout your code. It’ll help the 
reviewer and you’ll get fewer issues coming back.

## Getting started

If you don’t currently do code reviews, and you’re not using pull requests for contributing code, and you don’t have documented standards, 
all of the above might seem a little daunting.

Not having standards is a bit of a chicken and egg situation – without reviewing code, often preferences exist but aren’t expressed anywhere 
(some of our preferences have been implicit for years until a new contributor comes along and does something off the wall, and we realise it 
needs to be explicit). Consider using code review process for improving our standards and best practices – all new standards must 
be accepted by at least two colleagues, and all best practice suggestions must get at least one +1. This is intended to ensure that no one 
feels that standards are imposed upon them.

One way to start might be to just ask a colleague to give you feedback on your recent commits. This might help to start discovering preferences, 
and then these can be documented. From there, you’ll likely find that code review tools provide a much easier way to provide feedback, because you 
can associate your comments with a line of code very easily.

If you're part of a team that does not conduct regular code reviews, suggest to the team leader that they consider code reviews in order to
improve the quality of the code. 

*Thanks to [SmartBear](https://smartbear.com/learn/code-review/best-practices-for-peer-code-review) for content and images*
