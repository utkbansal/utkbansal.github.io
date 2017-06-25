---
layout: post
title:  "Why do you even write tests?!"
excerpt: "I get this question thown at me a lot, so let's just address the elephant in the room..."
---


I get this question thrown at me *a lot*, so let's just address the elephant in the room...

There are two obvious reasons(or maybe not!) to write tests - 

* Writing tests for my code helps me ensure, with minimal effort, that the code I wrote **works properly** and doesn't break some other virtually unrelated feature in the codebase.

* It acts as an **alternate documentation** for developers. Tests define the baseline of what the code should be able to do and in absence of good documentation, help developers to get a better understanding of the code.


Heck, without tests, all you have is a pile of code that once worked for you. You can either test it manually over & over, after each change or *it will break* without you knowing. 

Coming back to my work on MDAnalysis, after a rather slow start, I've been able to do quite some work this week. I've got 7 PRs merged!

* [#1370](https://github.com/MDAnalysis/mdanalysis/pull/1370) **Break build packagewise** - This PR breaks the build into two parts that are run separately. The first part runs the unported modules using `nose` and the second runs the ported modules using `pytest`. In the end, the coverage data from both the runs are combined to give the final data. This is done to help me break down the porting efforts into smaller chunks and to keep track of coverage while I'm at it.

* [#1413](https://github.com/MDAnalysis/mdanalysis/pull/1413) **Port lib/test_util.py to pytest** - Ports the `lib` module to be discoverable by `pytest`.

* [#1414](https://github.com/MDAnalysis/mdanalysis/pull/1414) **Port coordinates module** - Ports the `coordinates` module to be discoverable by `pytest`. A small thing went wrong with this, the PR was accidentally merged while it was being worked upon due to an issue with coveralls. I'll be opening a new PR soon to check in the remaining work.

* [#1417](https://github.com/MDAnalysis/mdanalysis/pull/1417) **Port formats module to pytest** - Ports the `formats` module to be discoverable by `pytest`.

* [#1420](https://github.com/MDAnalysis/mdanalysis/pull/1420) **Port topology module** - Ports the `topology` module to be discoverable by `pytest`.

* [#1434](https://github.com/MDAnalysis/mdanalysis/pull/1434) **Port utils module to pytest** - Ports the `utils` module to be discoverable by `pytest`. My mentor, Richard added some sweet pytest improvements to a couple of files in the module too!

* [#1418](https://github.com/MDAnalysis/mdanalysis/pull/1418) **Run the pytest testsuite in parallel** - This PR brings support for parallel execution of test cases with the help of the `pytest-xdist` plugin.



With these PRs merged, I'm finally moving towards my proposed timeline and I hope by the time you hear from me again, I'll be ahead of it! That's all for now, let's end this post with a quote I absolutely adore...



> Code without tests is broken by design...
>
> \- Jacob (core contributor to Django)