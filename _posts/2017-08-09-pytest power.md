---
layout: post
title:  "pytest power"
excerpt: "It's been a while since I've been using `pytest` to write unit tests for my code. This blog post is an overview of what I think is the best feature of `pytest` - `parmetrize`."
---

It's been a while since I've been using `pytest` to write unit tests for my code. This blog post is an overview of what I think is the best feature of pytest - `parmetrize`.

`pytest.mark.parametrize` is one of the greatest features of pytest. At `MDAnalysis` we use it widely and wherever possible. This is what is looks like - 

```python
import pytest
@pytest.mark.parametrize("test_input,expected", [
    ("3+5", 8),
    ("2+4", 6),
    ("6*9", 42),
])
def test_eval(test_input, expected):
    assert eval(test_input) == expected
```

Basically, what `parametrize` lets you do is, check the same piece of code for different sets of inputs. This is one of the primary things we do while testing code - we check all the edge cases we can think of. The neat thing about `parametrize` is that it minimizes code duplication - you just list out the set of inputs you want to check against and it works!

And you can go crazy about parametrizing "things" - it works with functions and classes too. Its power and simplicity is greatly amplified when you use it with classes.

Let's say that you are building a library that can read/write data to a number of file formats. In that case, you have different classes for different formats and probably each class inherits from a base class.

```python
@pytest.mark.parametrize('format', (
    'Format1',
    'Format2',
    'Format3',
))
class BaseTest(object):
    def test_open(format):
        # Check if the file can be opened

    def test_write(format):
        # Check if we can write to the file

    def test_read(format):
        # Check if we can read the file
```

In the above code snippet, you check if all of your classes conform to the base API standard. Each method in this test class is run against all of the formats mentioned. **This is a single point of truth that guarantees consistancy between all the classes and is hence my favourite feature of pytest!**

Coming on to what I've been doing for the past few weeks, I've been using `parametrize` all over the `MDAnalysis` testuite! Over the last couple of weeks I got [34 PRs merged](https://github.com/MDAnalysis/mdanalysis/pulls?page=2&q=is%3Apr+author%3Autkbansal+is%3Aclosed+merged%3A%3E%3D2017-07-21&utf8=%E2%9C%93) in and have 10 more open as of today! Summer is coming to an end soon (Winter is coming!! :D) and so is GSoC. The next few weeks will be spent on wrapping up this project and making sure everything is merged before end of August. Catch you later.
