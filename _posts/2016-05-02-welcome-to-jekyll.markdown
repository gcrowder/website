---
layout: post
title:  "A pretty smart dumb programming language classifier"
date:   2016-05-02 16:48:53 -0400
categories: machine learning
---

I worked over the weekend on a [programming language classifier](https://github.com/gcrowder/programming-language-classifier) using Python and scikit-learn. This classifier can identify an arbitrary program if it's from a set of 15 programming languages:
- c
- c#
- clojure
- common_lisp
- haskell
- java
- javascript
- ocaml
- perl
- php
- python
- ruby
- scala
- scheme
- tcl


Once you've cloned the repository, you can run it against your own programs. Simply run `python3 classifier.py filename` from your command line.

I wrote this sample program in Python to illustrate:
{% highlight python linenos %}
import random


def sum_5_random_integers():
    return sum([random.randint(1, 101) for x in range(5)])


def main():
    print(sum_5_random_integers())


if __name__ == '__main__':
    main()
{% endhighlight %}
You can see that it predicts correctly:
![Sample.py output]({{ site.url }}/assets/sample_output.png)

Clone the repo and try it yourself. It's kinda fun.
