---
layout: post
title:  "Python | Class (1)"
date:   2019-01-04
excerpt: "How to make a class"
tag: [python]
comments: true
---

{% highlight python %}

class Planet:

    def __init__(self):
        self.name = 'Hoth'
        self.radius = 20000
        self.gravity = 5.5
        self.system = 'Hoth System'

    def orbit(self):
        return '{name} is orbiting in the {system}'.format(name=self.name, system=self.system)

hoth = Planet()
print('Name is: {name}'.format(name=hoth.name))
print('Radius is: {radius}'.format(radius=hoth.radius))
print('The gravity is: {gravity}'.format(gravity=hoth.gravity))
print(hoth.orbit())

{% endhighlight %}

> ### Result  
> Name is: 'Hoth'  
> Radius is: 20000  
> The gravity is: 5.5  
> Hoth is orbiting in the Hoth System  

---

#### 코드 설명

{% highlight python %}

class Planet:

    def __init__(self):
        self.name = 'Hoth'
        self.radius = 20000
        self.gravity = 5.5
        self.system = 'Hoth System'

    def orbit(self):
        return '{name} is orbiting in the {system}'.format(name=self.name, system=self.system)

{% endhighlight %}
 
클래스의 틀을 만들기 위한 선언이다.  
클래스는 생성(선언)되어야 사용이 가능하다.  
self 는 클래스 자신을 가르킨다.  
__init__(self)은 생성자로서 클래스를 실제로 생성할 때 자동으로 수행된다.  
orbit(slef)은 메소드로서 선언되었을대 수행된다.  

---

{% highlight python %}

hoth = Planet()

{% endhighlight %}

실제로 클래스를 생성한다. (= 객체를 생성한다.)

{% highlight python %}

print('Name is: {name}'.format(name=hoth.name))
print('Radius is: {radius}'.format(radius=hoth.radius))
print('The gravity is: {gravity}'.format(gravity=hoth.gravity))
print(hoth.orbit())

{% endhighlight %}

생성된 객체의 데이터/함수에 접근한다.

