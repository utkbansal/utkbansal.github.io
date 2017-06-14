---
layout: post
title:  "GSoC - The Beginning"
excerpt: "Last time I told you about my journey in the Open Source world and I mentioned getting selected for Google Summer of Code. Well, this post will be about it - about how I’ve spent my last copule of weeks with MDAnalysis."
---


Last time I told you about my journey in the Open Source world and I mentioned getting selected for Google 
Summer of Code. Well, this post will be about it - about how I've spent my last couple of weeks with MDAnalysis.

Let's begin with what my project is, well, this is what the excerpt says

> The objective is to implement this shift in a way that existing development work is not affected and to improve 
> performance of the existing test cases and to make it more maintainable in general.

So basically I'm tasked with porting the whole testing framework from nosestes (which is no longer under active 
development) to pytest. Basically, the project consists of three main parts - 

* **Eliminating `nose` as a dependency** - this involves porting the existing tests and plugins from nose to pytest.

* **Improving performance & bringing down the time taken by the TravisCI build** - while doing the task mentioned above, 
I'll be using a cool feature of pytest known as `fixtures`. Think of `fixtures` as a resource that a test needs to 
perform its task - it might be as simple as a temporary directory where we can write datafiles. Now fixtures in pytest 
are very powerful and will help me to _cache reusable resources_  so I will not have to initialize them again and 
again for each test and this will help me bring down the total 
execution time.

* **Refactoring the code at a few places to make it more maintainable** - there are a couple of places in the codebase 
that are crying out to be refactored, one of them are the `Reader` classes. These classes can be refactored to inherit 
from a `BaseReader` class which can have all the basic functionality of the readers and then format specific readers 
can build upon this. This will serve us three purposes - first the lines of code will decrease, hence lower maintenance 
will be required, second, all the readers will follow the same standard API (not the case currently) and third, the 
`BaseReader` class will have its associated tests which will serve as a baseline for all existing and future reader 
classes.

So currently I am working on the first point as mentioned and have made _very little_ progress so far. I started out
late, owing to health issues, but hope to cover up the time lost by the first evaluation deadline. It's week 3 today and 
I'm still stuck on week 1, which is _really bad_, bad to the point that I think I might fail the first evaluations which are due 26th of this month. 

I've been working on splitting the TravisCI build to work with nose and pytest simultaneously and merge coverage, see [#1370](https://github.com/MDAnalysis/mdanalysis/pull/1370) and trust me TravisCI can be a _pain_ to work with. I'm 
facing stalled builds almost everytime I push code, which actually wastes a lot of time - 50 minutes to just figure 
that the build has stalled and then I have to restart it 3-4 times atleast to make it work. So it can take me up to 3 
hours just to verify if what I have done is correct or not.

Hopefully I'll be able to get back to my proposed timeline and you'll keep hearing about my journey with MDAnalysis. 
Cheers.