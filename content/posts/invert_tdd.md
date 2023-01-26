---
title: "Invert_tdd"
date: 2023-01-26T11:22:41-08:00
draft: false
---

# TDD Tip: Invert your assertion

One top tip I picked up years ago from a co-worker was to invert your assertions when you are in the midst of your TDD cycles. 

In other words, if you have an RSpec assertion like this:

expect(foo.nil?).to be_truthy

flip the truthy to falsey and run the test

expect(foo.nil?).to be_falsey

What you want to see there is that your test fails. In a 'true' TDD environment the test would be perfectly clean and no state would be acting on your subject, but that's just not how most test suites for production products work. 

Next time you think your tests are green, invert your assertion, run it, and make sure you don't have a false positive.
