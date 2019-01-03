---
layout: post
title:  "Python 3 for"
date:   2019-01-03
excerpt: "How to use 'for'"
tag: [python]
comments: true
---

# python for


> fruits = ['apple', 'orange', 'strawberry', 'watermelon']

{% highlight python %}

for fruit in fruits:
    print(fruit)

{% endhighlight %}

* apple
* orange
* strawberry
* watermelon

---

{% highlight python %}

for fruit in fruits[1:3]:
    print(fruit)

{% endhighlight %}

> watermelon
> orange
> strawberry

---

{% highlight python %}

for fruit in fruits:
    if fruit == 'strawberry':
        print('{} - favorite'.format(fruit))
        break
    else:
        print(fruit)

{% endhighlight %}

* apple
* orange
* > strawberry - favorite




