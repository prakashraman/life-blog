Nowadays writing test cases has become more of a practice which doesn’t which is not supported by a strong reason. However even though most teams implement this practice, is seems slightly unfounded or is based on reasons not strong enough. Either way, it still contributes a huge value to software quality and software development.

#### Test Suite Strategy

The goal of having test cases varies from project to project, of course. So what could the strategy of a test suite be in the case, say, of a professional project? And what it could it be for a personal project on Github?

#### Professional Projects

I count all repositories we work on, as part of our job, to be professional projects.

Most of the the repos we work on at work are part of a larger eco-system of sub-systems which interact with each other quite closely (e.g a micro service/module which handles database operations OR a library which governs interfacing with an API system).

I would prefer to have a more elaborate E2E testing framework (over having unit tests), a suite that tests all the sub-systems of the product together. In other words, I would test if all the sub-systems are behaving themselves, and if it's predicable. However, most of the time, we don't have an E2E suite in place, or even if we start with one, it quite quickly gets abandoned during the product development roadmap.

Therefore yes! We **have** to write unit tests! So what sort of tests should we write? Let's read on ...

#### Personal Projects

Strategies for personal projects need to be well though out unit tests, as most of the time personal projects comprise of 1 or 2 systems working together. And we should be able to get by just writing well thought out unit-tests.

#### What test cases should cover

Test cases should cover those harder to execute logic of code; or code that gets executed very rarely. In every application/product/micro-service, we will always have a good amount of code that does not get executed in normal usage.

e.g 
```
1. Last "page" of a pagination set
2. First view post user registration
3. The thank-you/confirmation-page on purchase completion
```

When I write test cases my intent is to be able to simulate an actual human interaction or usage of your product.

When we write code we consider the positive and negative cases and sometimes we even a few edges cases. However when we are in a development team (and no testing team) it is very easy to skip a few or even many use cases (not edge cases, but actual use cases) as we think someone else in the team might cover it, no real decision was made on what the test cases should cover, etc. Therefore most of time, we land up writing the most straight forward test case which probably gets covered by usual usage anyway.

A different way to look at things, maybe, writing test cases is a chance to think like a regular user and to write test cases for way they might, in reality, use the application.

e.g 
```
1. Double swiping on the final swipe
2. Multiple clicks on a button
3. Leading/trailing spaces in passwords
4. User's switching time zones
5. Opening an app when there is not internet
```

#### Code Coverage

Such a touchy topic sometimes :) Well, I personally don't care much for a min code coverage a project must abide. However, when the team decides to have a particular minimum, we must play nice! We should first just write all the test cases we would want to include, and then check what the coverage is; we should not write test cases to reach a coverage (but yes, I know! It happens sometimes!)

That being said, when I see developer libraries that can included in my project, I'd love to know that library has 100% code coverage. 

So, yeah, if I am going to put up a library that the world can install and use. I'd just do that little extra and showcase that "100% code coverage badge!"