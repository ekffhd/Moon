---
layout: post
title: Python | map() function
date: 2019-01-05
excerpt: "How to use map()"
tag: ['python']
comments: true
---

{% highlight python %}

from random import shuffle

def jumble(word):
    anagram = list(word)
    shuffle(anagram)

    return ''.join(anagram)


words = ['beetroot', 'carrots', 'potatoes']
anagrams = []

# (1)
for word in words:
   anagrams.append(jumble(word))
print(anagrams)

# (2)
print(list(map(jumble, words)))

# (3)
print([jumble(word) for word in words])

{% endhighlight %}

> ### Result  
> ['rtobeeot', 'rrsotac', 'psetoota']  
> ['rtboeeto', 'rtocasr', 'taopetso']  
> ['btoretoe', 'carrtos', 'estatpoo']  
> 
> ( 위의 결과값은 랜덤값입니다. )   

---  
  
## 코드 설명

(1) basic

{% highlight python %}
for word in words:
   anagrams.append(jumble(word))
print(anagrams)
{% endhighlight %}

(2) map(function, item)

{% highlight python %}
print(list(map(jumble, words)))
{% endhighlight %}

(3) list comprehension

{% highlight python %}
print([jumble(word) for word in words])
{% endhighlight %}

> 위의 세 구문은 의미가 같다.



