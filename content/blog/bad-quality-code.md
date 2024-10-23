+++
date = '2024-10-21T23:16:47+03:00'
draft = true
title = 'Bad Quality Code'

tags = ['quality-code']
categories = ['code-philoshopher']

[params]
    author = 'George Karampelas'
    wikipedia = 'https://en.wikipedia.org/wiki/Bruce_Willis'

+++

As a programmer the last one and a half year, I am gonna say about something that everyone codes have said. Bad quality of code, yep that's my topic. I am consider as the newest and lower seniority on my team, but after one and a half year of my career on the same project I miss my first days of just coding. Why? Because after some time of "PURE" implementation, testers found some bugs, something broken on production, change request from the client etc. Most of the times the problem is so small, bad quality of code that it is not readable maintainable and editable, for that reason you waste more time to understand the code than understand what the client asked again.

Let's talk with an example, you want to create a service that handle all the business logic of an entity and for one action this entity has numerous scenarios. As I believe it is a bad practice to use just a switch and split the code on numerous private methods to make the code look good, it is not. Do you know why?

- I can't read it

- I can't maintain it

- I can't test it

- I can't extend it

- I can't reuse it

- I can't document it

For all these reasons it would be better to split this business logic one more services if it is necessary or you can use Strategy Pattern. Feel free to explore the huge world of programming.

As I like, I code with TDD so I try to code the way I can test, obviously not using @Autowired. I write my basic scenarios with empty methods that I am gonna implement after my basic tests I start implement as I go my code is ugly and not perfect or acceptable for a merge request, but it works it passes the tests then I refactor my code to be more readable, maintainable and editable as the tests are green.