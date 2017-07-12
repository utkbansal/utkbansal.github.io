---
layout: post
title:  "Hey there bots!"
excerpt: "At this point of time, I've started to wonder if anyone even reads my blog. Am I just throwing stuff into a black hole?! *Are you there? Are you human?*"
---

At this point of time, I've started to wonder if anyone even reads my blog. Am I just throwing stuff into a black hole?! *Are you there? Are you human?* There are a couple of bots that do visit my site every once in a while though. I think one of them is Google's crawler. I wonder if someday, in the not so distant future, these bots will talk to me. They certainly know me well... Probably more than you know me! 

Anyways, let's talk code. I had evaluations last month. And I received some positive feedback from my mentors! Shift to `pytest` is almost done - only one class in the `analysis` module is left to be ported. I have also been working on refactoring the `utils` module to use `pytest` conventions and features - which brings us to Phase 2. 

Basically, **Phase 2 is all about refactoring the test suite to follow the `pytest` style of doing tests.** It basically involves -

* Getting rid of all `TestCase` inheritance
* Using `fixtures`
* Using `parametrize`
* And using more `pytest` goodness like `asserts`, `raises` helper, `warn` helper, etc.

I also have a couple of PRs that were merged/are in progress over the last couple of days

* [#1472](https://github.com/MDAnalysis/mdanalysis/pull/1472) **Pytest Style: test_streamio.py**(WIP)
* [#1470](https://github.com/MDAnalysis/mdanalysis/pull/1470) **Pytest Style: test_persistence.py**(WIP)
* [#1469](https://github.com/MDAnalysis/mdanalysis/pull/1469) **Pytest Style: test_nuclinfo.py**(WIP)
* [#1468](https://github.com/MDAnalysis/mdanalysis/pull/1468) **Pytest Style: test_modelling.py**(WIP)
* [#1467](https://github.com/MDAnalysis/mdanalysis/pull/1467) **Pytest Style: test_log.py**(WIP)
* [#1450](https://github.com/MDAnalysis/mdanalysis/pull/1450) **Port analysis module to pytest**(WIP)
* [#1473](https://github.com/MDAnalysis/mdanalysis/pull/1473) **Pytest Style: test_imports.py**(Merged)
* [#1471](https://github.com/MDAnalysis/mdanalysis/pull/1471) **Pytest Style: test_selections.py**(Merged)
* [#1466](https://github.com/MDAnalysis/mdanalysis/pull/1466) **Pytest Style: test_deprecated.py**(Merged)
* [#1465](https://github.com/MDAnalysis/mdanalysis/pull/1465) **Pytest style: test_datafiles.py**(Merged)
* [#1464](https://github.com/MDAnalysis/mdanalysis/pull/1464) **Pytest Style: test_altloc.py**(Merged)
* [#1443](https://github.com/MDAnalysis/mdanalysis/pull/1443) **Port core module to pytest**(Merged)
* [#1441](https://github.com/MDAnalysis/mdanalysis/pull/1441) **Fix coverage drop in coordinates module**(Merged)
* [#1439](https://github.com/MDAnalysis/mdanalysis/pull/1439) **Port auxiliary module to pytest**(Merged)


That's pretty much it. See ya later. Cheers!
