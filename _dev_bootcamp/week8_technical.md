---
layout: page
title: TDD, taking the interpretive out of the dance.
---

DDH recently challenged the Ruby on Rails community's assumptions regarding adoption of Test Driven Development. His arguement was, essentially, that putting too much emphasis on the tests has a cost in other areas.

There are however, certain things that you really want to know are what they proport to be. It may seem like a silly example, but testing that your variables are the type you expect them to be is important. If you are handling data where it matters; and frankly, who isn't? it is important to validate your data and test that your recent changes haven't done any harm.

But that isn't the best reason for tests. Testing is an exercise in expressing yourself clearly, first of all to yourself and then to any programmer who might come across your code. It is a way of communicating exactly what you expected to have happen in this chunk of code.

To communicate what you want to have happen _clearly_ you need to actually have a pretty good idea of _what_ you want to have happen. TDD forces you to get clear on your intent. It has the added side benefit of expressing your intent for future developers. **(The future developer you help may just be yourself!)**

DHH does have a valid concern. Test Driven Development can be the tail that wags the dog if you think of it religiously. It isn't salvation unto itself. It is the process you take to get from red to green that provides you opportunities to do things a liitle better. But if you put too much focus on the tests, you might stiffle your creativity, and that would be terrible.

Test Driven Development is a tool, hopefully one of many that you will use in your career. Use it, master it, but do not think that there is salvation in doing so. Use Test Driven Development to give yourself a lot of opportunities to be clear and write better code.

