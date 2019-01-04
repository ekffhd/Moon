---
layout: post
title:  "Python | Class (2)"
date:   2019-01-04
excerpt: "How to make a class"
tag: [python]
comments: true
---

{% highlight python %}

class Planet:
    
    # class attribute
    shape = 'round'
    
    # initializer
    def __init__(self, name, radius, gravity, system):
    
        # instance attribute
        self.name = name
        self.radius = radius
        self.gravity = gravity
        self.system = system
        
    # instance methods
    def orbit(self):
        return '{name} is orbiting in the {system}'.format(name=self.name, system=self.name)
        
    # class methods
    @classmethod
    def commns(cls):
        return 'All planets are {shape}'.format(shape=cls.shpae)
        
    @staticmethod
    def spin(speed='2000 mile per hour'):
        return 'The planet spins and spins at {speed}'.format(speed=speed)
        
X = Planet('Hoth', 20000, 5.5, 'Hoth System')

print(X.shape)
print(Planet.shape)

print(X.name)
# print(Planet.name) << wrong expression

print(X.orbit())
# print(Planet.orbit()) << wrong expression

print(X.commons())
print(Planet.commons())

print(X.spin('a very high speed'))
print(Planet.spin('a very low speed'))

{% endhighlight %}

> ### Result  
> round  
> round  
> Hoth  
> Hoth is orbiting in the Hoth  
> All planets are round  
> All planets are round  
> The planet spins and spins at a very high speed  
> The planet spins and spins at a very low speed  
  
  
## 코드 설명

> ### 요약  
> class ooo : 객체를 색성하지 않아도 사용할 수 있다.  
> instance ooo : 반드시 객체를 생성해야 사용할 수 있다.
  
  
* __class attribute (클래스 속성)__  
클래스 객체를 생성하지 않아도 접근할 수 있다.

{% highlight python %}

# 객체 생성
X = Planet('Hoth', 20000, 5.5, 'Hoth System') 

# 객체로 접근
print(X.shpae)

# 클래스로 접근
print(Planet.shape)

{% endhighlight %}
  
  
* __instance attribute (인스턴스 속성)__  
객체에서만 접근이 가능하다.

{% highlight python %}

# 객체로 접근
print(X.name)

# 클래스로 접근
# print(Planet.name) << wrong expression

{% endhighlight %}
  
  
* __class method__ & __static method__  
클래스 객체를 생성하지 않아도 접근할 수 있다.

{% highlight python %}

# class method
# 객체로 접근
print(X.commons())

# 클래스로 접근
print(Planet.commons(None))

# static method
# 객체로 접근
print(X.spin('a very high speed'))

# 클래스로 접근
print(Planet.spin('a very low speed'))

{% endhighlight %}
  
> class method 와 static method의 차이는 추후의 포스트로 올릴 예정

