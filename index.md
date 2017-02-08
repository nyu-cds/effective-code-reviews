---
layout: lesson
root: .
---
A *code review* is a process of consciously and systematically examining source code for mistakes, and to improve
the overall quality and maintainability of the code. Code reviews 
(in contrast to [*code inspections*](http://www.methodsandtools.com/archive/archive.php?id=66)) 
have been 
repeatedly shown to accelerate and streamline the process of software development like few other practices can. 
There are peer code review tools and software, but the concept itself is important to understand. Software is written by
human beings. Software is therefore often riddled with mistakes. To err is, of course, human, so this
is an obvious correlation. But what isn’t so obvious is why software developers often rely on manual or 
automated testing to vet their code to the neglect of that other great gift of human nature: the ability 
to see and correct mistakes ourselves. 

Code reviews look for the following:

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