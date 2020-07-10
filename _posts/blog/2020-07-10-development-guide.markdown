---
date:   2020-07-10 23:00:00 +0200
layout: single
title:  "Development Guide"
---
As a software engineer, one of my pet peeves is dealing with the almighty developer guide. This document exists at almost every software company as an aid for developer writing code. Among other things, it outlines rules for the formatting of code.

These guides are important, and necessary, if mainly as a learning tool for developers to recognize features of the tools and languages used. The guide also serves as a warning against potentially undesirable side effects or pitfalls which may not be obvious at first glance. Used in the right way, developers can learn and debate the merits of developing a certain way.

Sadly, too often the developer guide becomes a way for one person to decide every detail of how the code should look. The guide then goes beyond merely avoiding bad code construction, and delves into enforcing the spacing of the code, the format, and many tiny details.

I have actually heard people defend developer guide rules such as "The code should be self-evident and have minimal comments". The next day I'll be attempting to understand several portions of code which appear to me to be hopelessly tangled. After 30 minutes spent analyzing 50 lines of code, I opt to ask the developer who wrote the code three months ago what it does, and he will spend another thirty minutes deciphering it all over again.

The silly developer guide rules don't help. To me, the developer guide should primarily be used to avoid problems. Very few projects suffer from too many comments in the code. This rule just served to pump our egos up in thinking we were putting out code so good it didn't need comments, which was not true.

Intertwined in the developer guide are the tools which are often used to enforce good coding practices. This could be a helpful thing to have in the project, but it all depends on the tool used, and how it is used. I once worked on a project that used a project called [standard][standard]. I had a real problem with it. The philosophy behind it was that instead of debating the merits of one way of doing things over another, this tool would simply set the terms. At best, we could ignore a rule in certain cases. There was no customization beyond that.

Instead of this centralized dictatorship of code formatting, consider the well-known tool [ESLint][eslint], which allows for extensize configuration, as well as having an option to use a list of recommended rules, to facilitate a quick start when desired. I think that the time spent discussing these points is important. It gets developers in the mindset of developing in an abstract, flexible fashion that allows a team to work on the same code seamlessly. The goal shouldn't be to remove individual creativity, but rather to encourage it when it makes sense.

I think the age-old debate of Tabs vs Spaces is an example of this difference of philosophy. It makes no sense to me that there seem to be more developers who prefer to indent their code using spaces as opposed to tabs. This might have made sense over ten years ago, when some text editors didn't have proper configuration options for indentation. Now I can configure any respectable editor to display a `TAB` character as a certain number of columns.

So what is the debate? If I want my editor to use 17 columns for every `TAB` character, that's my business. When I commit the code to the repository, someone else can grab it and use their own configuration to determine how many columns a `TAB` character uses. That's the flexible option. Using spaces just means that we can mandate 2-space indentation, and use that to attempt to develop code with too many nested levels of logic to be easy comprehensible. Let's stop micromanaging developers and instead just mark the danger areas and let them be free otherwise.

[eslint]: https://eslint.org/
[standard]: https://github.com/standard/standard