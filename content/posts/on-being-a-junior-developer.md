---
title: "On Being a Junior Developer"
date: "2012-11-20"
categories: 
  - "software engineering"
tags: 
  - "software engineering"
  - "career development"
---

Junior developer (for purposes of this post)is a developer with < 2 years experience programming in industry who have an interest in sharpening their technical skills.

I recently graduated from Stanford with a degree in Computer Science. I've been programming for 4 years and feel comfortable claiming ~1.5 years industry experience through summer internships, failing as a solo founder, being a lead engineer for a startup, various freelance gigs, and my current position at a mobile health startup I helped found in December. What follows is the list I wish someone had written for me as a developer starting out in the tech industry:

# 1) Read other people's code

Perhaps the best way to enhance your technical ability is to directly read other people's code. [Github](http://github.com "Github") is a fantastic resource; and it's even better if you have an all star developer already within your work environment that you can bounce questions off of. Here are two things I think are particularly valuable:

Focus on naming conventions; good programmers define variables with names that enhance the readability of the code and also provide intent, but also don't couple the variable name to a certain data structure type.

Try to load the whole system into your head and understand it. Notice how the various components are decoupled, design patterns, and also how they have spelled out their unit tests. Holding well designed systems in your head is very much like visualization within athletics. Visualizing yourself in a certain athletic situation or doing a specific technique correctly has been linked to improved performance. Do it for coding too.

# 2) Plan things out

Before you ever start coding you should sit down with a whiteboard or pen and paper. These drawings don't have to be complex, but should provide you with a holistic view to how all of the components you are about to code or touch should interact. In addition you should be exploring different design choices at this stage, it's much easier to erase a whiteboard and start from scratch then be a week into your coding and realize what a mess things have become due to lack of planning.

# 3) Have an opinion

As a junior developer you should have opinions and you should have reasons as to why you have that opinion. Even asking yourself the question of "why did you make choice X?" as a thought experiment is a nice way to have a robust answer and solution to your problem. The reason you need to have opinions instead of simply following along is because you are literally learning into understanding. Ask yourself the tough questions so that when a senior developer reviews your code you have a legitimately robust solution.

# 4) Ask questions

In the very early days of my current startup the backend developer wrote an abstract base class for all of our Models in Django, which essentially acts as our very own wrapper on the Django ORM. I was reading over his code and was very curious as to why he had gone through the trouble of doing this.. after all isn't that what an ORM is designed for? His answer:

"I did that because it makes it easy for us to change the underlying database without having huge migration issues".

He had been bitten hard by database migration issues before (in particular a postgres to noSQL solution) and was prudent enough to take preventative action.

Ask questions about peculiar things, there is often wisdom and learning to be had.

# 5) Explore new technologies

One of the more unfortunate trends I see with some of my graduating Stanford CS friends is that they are often afraid to try new technologies. They have a computer science degree, not a 'programming for industry' degree and it terrifies them a little bit. All Stanford people have known while growing up is being the top of their class and naturally gifted. When confronted with a situation they aren't good at they often freeze up for fear of failure. As a junior developer it is in your best interest to fight those instincts and cast your net far and wide. Every piece of technology you touch influences you in some way, and having used various technologies exposes you to new paradigms and ways of doing things. Touching a new technology / programming language is expanding your 'world view' of programming.

Note: The classic debate is functional vs OOP; however even something as small as giving [Node.js](http://nodejs.org "Node.js") a try can have benefits. After playing around with [Node.js](http://nodejs.org "Node.js") I now generally use their two part callback for asynchronous code because I really like that decoupling.

# 6) Embrace unit testing

One thing I didn't do enough of at Stanford was unit testing. I had one TA who bugged me to do it (I still didn't); however the rest of my classes never did. We weren't graded on unit tests and we got to reset our projects every 10 weeks. University just isn't built for cultivating a testing culture.

As a junior developer you really do need to embrace unit tests. I will advocate for Test Driven Development (TDD) not only because it improves my confidence that my code is functioning properly but has also really improved my function prototypes as I generally 'call' the function before its even built. I'm not particularly fond of BDD; however any form of testing you can do is better than nothing (trust me when it comes for v 1.1 of your app you'll want those regression tests too).

# 7) Refactor

One of the problems of being a junior developer is that you haven't been in industry long enough to be bitten by poorly written code that becomes impossible to maintain. Being a developer isn't about writing code, it's about producing working software while simultaneously hitting business goals and maintaining expectations. When you start with a blank slate everything is golden: you get to build from the ground up, features get spun out faster because they don't interact with other parts of the system as much and the sky is the limit. If you are simply slinging code without any regard to maintainability, after about 6 months you will have accumulated a huge pile of technical debt. New features can't get put out as fast, it takes longer to know what a certain function does and changing one thing wreaks havoc on another component of the system. Unfortunately the demand for new features from your users doesn't simply decline with your technical debt; in fact it is likely increasing. This puts developers in a bad spot because they have a tangled pile of code and non technical folks requesting new features at rapid fire pace who have no idea what it means when you say 'spaghetti code'.

So what happens next? The developers say the old system is slow and everything would magically be better if only we could rewrite the thing from scratch. So new developers are brought on to maintain the old stack and your 'best' developers begin creating the system from scratch. Bottom line... this is a huge waste of resources and doesn't work anyways (it always takes longer to rewrite than you think, the new stack is always trying to catch up with the old stack, lots of QA time, etc).

But here's the kicker, who wrote the initial version in the first place? **Developers.** 

I want you to imagine for a second a business development employee approach you and say "Yeah, that old partnership that is supposed to be our flagship deal is slow and I messed up that relationship pretty bad. Don't worry though, if we go get another partnership while still trying to string the old one along we can be back to full speed!". That's unprofessional, and frankly so is unmaintainable code.

The solution to this is preventative medicine. As a developer you should be constantly rewriting and refactoring your code. Don't ever check in code that isn't a little better off than before you started. Maintainable code is code that is easily readable, extendable, and testable by outside developers.

Unless you have a very very good reason to put in that 'quick fix' don't ever sacrifice a local maxima of productivity for the long term health of your codebase.
