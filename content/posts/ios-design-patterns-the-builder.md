---
title: "iOS Design Patterns: The Builder"
date: "2016-01-05"
categories: 
  - "software engineering"
tags:
  - "software engineering"
---

One of the things I'd like improve in 2016 is my knowledge of software engineering design patterns, with a particular emphasis on iOS. I'll be posting a quick summary of each one I stumble across on the blog so that my future self can find things again easily.

Today's pattern is called ['The Builder'](https://en.wikipedia.org/wiki/Builder_pattern). The intent of the pattern is to make it easy to create objects with a lot of initial configurations, without bloating your code with a bunch of long initializers. The main difference between the builder and the factory design pattern is the complexity of the object being created ([great answer here](http://stackoverflow.com/questions/3687299/abstract-factory-factory-method-builder)).

[The Builder Pattern in Objective-C](http://www.annema.me/the-builder-pattern-in-objective-c), by Klass Pieter provides an excellent example implementation. Creating an object with his builder implementation looks like this:

Pizza \*pizza = \[Pizza pizzaWithBlock:^(PizzaBuilder \*builder\]) {
    builder.size = 12;
    builder.pepperoni = YES;
    builder.mushrooms = YES;
}\];

I encourage you to read the whole post for further details and to keep this one in your back pocket the next time you type out multiple, magnificently long initializers.
