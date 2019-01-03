---
layout: post
title:  "Python | Defining functions"
date:   2019-01-04
excerpt: "How to define functions"
tag: [python]
comments: true
---


{% highlight python %}

 def greet(name, time):
     print('Good {time}, {name}! hope you are well'.format(name=name, time=time))


name = 'shelly'
time = 'morning'

greet(name, time)

{% endhighlight %}

> ### Result  
> Goom morning, shelly! hope you are well  

---

## Set initial value

{% highlight python %}

def greet(name = 'shelly', time = 'morning'):
    print('Good {time}, {name}! hope you are well'.format(name=name, time=time))
    
greet()

{% endhighlight %}

> ### Result  
> Goom morning, shelly! hope you are well  
