---
layout: post
comments: true
date: 2019-11-19
title: "Lamda Expression"
description: "람다식에 대하여 알아보자!"
subject: blog
permalink: /post/csharp/lambda/
categories: [C#]
tags: [C#, Lambda, Expression]
---
# Lambda Expression(Statemet)



## 요약
프로그래밍 언어에서 사용되는 개념. 익명함수(Anonymous function)를 지칭하는 용어. 주로 고차함수의 인자(argument) 혹은 결과값으로 사용됨.


## 람다식의 형태
* Expression lambda (람다식)

~~~csharp
void foo()
{
    (params) => func;
}

void func(object param)
{
    // 구현
}
~~~

* Statement lambda (람다문)

```csharp
void foo()
{
    (params) => 
    {
        //구현
    };
}
```

## 장점
* Code의 간결성

```csharp
// 기본 
int f()
{
    int result = 0;
    for (int i = 0; i < 10 ; ++i) 
    {
       ++result;
    }

    return result;
}

void sum10()
{
    int i = f();
    Console.WriteLine(i);
}

// 출력 : 10
```


```csharp
// 람다
void sum10()
{
    Console.WriteLine(() =>
    {
        int result = 0;
        for (int i = 0 ; i < 10; ++i)
        {
            ++result;
        }

        return result;
    });
}
// 출력 : 10
```

