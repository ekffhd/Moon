---
layout: post
title: Python | List Comprehensions
date: 2019-01-05
excerpt: 리스트의 확장된 사용법
tag: [python]
comments: true
---

{% highlight python %}

prizes = [5, 10, 50, 100, 1000]

double_prizes1 = []

for prize in prizes:
    double_prizes1.append(prize*2)

print(double_prizes1)


# comprehension method

double_prizes2 = []

double_prizes2 = [prize*2 for prize in prizes]

print(double_prizes2)

{% endhighlight %}

> ### Result  
> [10, 20, 100, 200, 2000]  
> [10, 20, 100, 200, 2000]  

## 코드 설명

(1)   
{% highlight python %}
for prize in prizes:  
    double_prizes1.append(prize*2)  
{% endhighlight %}

(2)  
{% highlight python %}
double_prizes2 = [prize*2 for prize in prizes] 
{% endhighlight %}

위의 두 구문은 같은 의미이다.  
  
  
  
{% highlight python %}

nums = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

squared_even_nums1 = []

for num in nums:
    if(num ** 2) % 2 == 0:
        squared_even_nums1.append(num ** 2)

print(squared_even_nums1)


# comprehension method
squared_even_nums2 = []
squared_even_nums2 = [num ** 2 for num in nums if(num ** 2)%2 == 0]

print(squared_even_nums2)

{% endhighlight %}

> ### Result  
> [4, 16, 36, 64, 100]  
> [4, 16, 36, 64, 100]  

## 코드 설명

(1)

{% highlight python %}
for num in nums:
    if(num ** 2) % 2 == 0:
        squared_even_nums.append(num ** 2)
{% endhighlight %}

(2)

{% highlight python %}
squared_even_nums = [num ** 2 for num in nums if(num ** 2)%2 == 0]
{% endhighlight %}

위의 두 구문은 같은 의미이다.

