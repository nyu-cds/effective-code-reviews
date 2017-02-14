---
title: "Introduction to Code Reviews"
teaching: 5
exercises: 0
questions:
- "Why do code reviews?"
- "When and how do they happen?"
objectives:
- "Gain an understanding code reviews and why they are important."
keypoints:
- "Code reviews ensure consitent quality across the team"
- "Code reviews help avoid errors"
- "There are many tools for code reviews"
- "Social version control platforms also provide tools for code reviews"
---

### Why do code reviews?

Constructive code reviews are a means of ensuring the quality of code is consistent across the team – and typically all 
code gets raised to a much higher standard as a result. 

Through code reviews, team members can obtain feedback from their 
peers on their contributions before merge, as well as learn from the feedback on other colleagues’ contributions. 

Code review also promotes a shared understanding of the entire codebase amongst the team, making it easier for everyone to 
contribute. Additionally it provides visibility of changes to the codebase to everyone, which helps to avoid errors, and 
reduce wasteful or overly complicated code being added to the codebase.

### When should code reviews happen?

Code reviews should happen before any commit gets merged into a production codebase. Sometimes this principle needs to be 
bypassed (e.g. an emergency fix for production when no reviewer is available) but such changes should be still be reviewed retrospectively.

Ideally, code would undergo some kind of *continuous integration testing* prior to review. This is where a series of tests is run
against the code to ensure that it is still functioning correctly after the change. The sophistication of such 
testing can range from basic syntax checking up to full-scale test deployments. If it passes this automated checking, 
then it’s worth spending human effort on a review.

### Where do code reviews happen?

Most social version control platforms (Github, Bitbucket, etc.) have the ability to do Pull Requests (or Merge Requests in Gitlab’s case). 
This is the easiest (but not necessarily most robust) way to have them.

Dedicated code review platforms such as Gerrit or Crucible may also be used – it doesn’t really matter what tool you use as long 
as you are able to comment at the line level, at the general level, and provide some indicator of approval (e.g. a +1 or shipit)

### What do code reviews look for?

* Feature completion - making sure that the code meets the requirements
* Potential side effects - seeing if the changed code causes any issues with other features
* Readability and maintainability - ensuring the code is readable and conforms to 
[clean code principles](http://www.goodreads.com/book/show/3735293-clean-code)
* Consistency - checking that the code conforms to the team coding style
* Performance - assess if the code requires optimization
* Exception handling - make sure bad input and exceptions are handled correctly
* Simplicity - determine if there are simpler or more elegant alternatives available
* Reuse - check to see if the functionality is reusing existing code
* Testing - ensure that enough test cases have been provided to ensure good coverage