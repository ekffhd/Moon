---
layout: post
title: Python | filter() function
date: 2019-01-05
excerpt: How to use filter()
tag: [python]
comments: true
---

{% highlight python %}

def remove_fails(grade):
    return grade != 'F'
    

grades = ['A', 'B', 'F', 'C', 'F', 'A']

filtered_grades = []

# (1)
for grade in grades:
    if(grade != 'F'):
        filtered_grades.append(grade)
print(filtered_grades)

# (2)
print(list(filter(remove_fails, grades)))

# (3)
print([grade for grade in grades if grade != 'F'])

{% endhighlight %}

> ### Result
> ['A', 'B', 'C', 'A']  
> ['A', 'B', 'C', 'A']  
> ['A', 'B', 'C', 'A']  

## 코드 설명
  
  ---
  
(1) for loop
{% highlight python %}
for grade in grades:
    if grade != 'F':
        filtered_grades.append(grade)
print(filtered_grades)
{% endhighligh %}
  
(2) filter(functions, item)
  
{% highlight python %}
print(list(filter(remove_fails, grades)))
{% endhighligh %}

'functions'에 들어가는 함수는 'true'/'false' 를 반환해야한다. 
리스트 grades의 원소들을 remove_fails 함수에 인자값으로 넘겨주고 반환값이 'true'인 것만 '필터'해준다.

(3) list comprehension
{% highlight python %}
print([grade for grade in grades if grade != 'F'])
{% endhighligh %}

> (위의 세 구문은 같은 의미이다.)
