---
layout: post
title: "Python 3 format()"
date: 2019-01-03
tags: [python]
comments: true
---

# python format()

<code>

num1 = 3.1425243
num2 = 10.290394


print('num 1 is', num1, 'and num 2 is', num2)
#num 1 is 3.1425243 and num 2 is 10.290394


print('num 1 is {} and num 2 is {}'.format(num1, num2))
#num 1 is 3.1425243 and num 2 is 10.290394

print('num 1 is {1} and num 2 is {0}'.format(num1, num2))
#num 1 is 10.290394 and num 2 is 3.1425243


print('num 1 is {0:.3} and num 2 is {1:.3}'.format(num1, num2))
#num 1 is 3.14 and num 2 is 10.3

print('num 1 is {0:.3f} and num 2 is {1:.3f}'.format(num1, num2))
#num 1 is 3.143 and num 2 is 3.143

print(f'num 1 is {num1:.4f} and num 2 is {num2:.4f}')
#num 1 is 3.1425 and num 2 is 10.2904

</code>

{% highlight python %}

num1 = 3.1425243
num2 = 10.290394


print('num 1 is', num1, 'and num 2 is', num2)
#num 1 is 3.1425243 and num 2 is 10.290394


print('num 1 is {} and num 2 is {}'.format(num1, num2))
#num 1 is 3.1425243 and num 2 is 10.290394

print('num 1 is {1} and num 2 is {0}'.format(num1, num2))
#num 1 is 10.290394 and num 2 is 3.1425243


print('num 1 is {0:.3} and num 2 is {1:.3}'.format(num1, num2))
#num 1 is 3.14 and num 2 is 10.3

print('num 1 is {0:.3f} and num 2 is {1:.3f}'.format(num1, num2))
#num 1 is 3.143 and num 2 is 3.143

print(f'num 1 is {num1:.4f} and num 2 is {num2:.4f}')
#num 1 is 3.1425 and num 2 is 10.2904
{% endhighlight %}

