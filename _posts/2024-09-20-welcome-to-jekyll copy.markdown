---
layout: post
title: 'Say "Pytest Test" One More Time'
date: 2024-09-20 00:21:41 +0200
categories: til testing pytest coverage
---

![My helpful screenshot](/assets/testing.jpg)

Tests are important! Not just as a safety net for any code-breaking changes you or a pesky colleague might push (on a Friday, of course). They also help you better understand the design of your features, their use, and their limitations.

When I started my development career, I spent a week writing tests for my first feature, until I'd become a self-certified Cypress ninja. What if there's a network error? What if the file is empty? What if the user headbutts the keyboard while the app is loading? Better write another test! Just to be sure, you know?

Now that I'm more experienced, I'm a bit more chill with my testing, but I'd still like to maintain good test coverage of the repository. A simple tool for automating such checks for your pytest tests ("pytest tests" — yep, that doesn't sound weird at all) is tools like `coverage` or the `pytest-cov` plugin.

As a wrapper around your `pytest` framework, they allow you to scan and see just how much of your code is shielded and protected by tests. Not only that, they have the ability to actually show you which lines are covered by testing and which cry for more attention. They also produce a really cute HTML report you can send to brag to all your friends, at least those who'd stay after "90% for app.py! Can you believe that?"

I think it's really cool to be able to introduce a coverage library into the `CI pipeline`, and always be on top of the current percentage of tested features. If you're feeling particularly devious, you can even set it to fail the pipeline if the percentage drops beneath a certain threshold. Or at least send a very stern reminder to your colleagues that TESTS ARE IMPORTANT!
