---
layout: post
title: "Builder Patten "
date: 2024-02-19 17:00:00 +0900
description:  # Add post description (optional)
img: java.png # Add image post (optional)
fig-caption: java, Design Pattern, Builder Pattern
---

## Builder Pattern 이란?

복잡한 객체를 생성하는 방법에 관한 디자인 패턴이다. 

이 패턴은 객체 생성 과정을 단계별로 나누어, 필요한 객체만을 생성하는 방법을 제공한다. 

Builder Pattern의 주요 목적은 객체의 생성과 표현 방법을 분리하여 동일한 생성 절차에서

서로 다른 표현 결과를 만들 수 있도록 하는 것이다.

<aside>
💡 Tip. Builder Pattern의 사용 효과

빌더 패턴(Builder Pattern)을 사용하게 되면 객체를 생성할 때 
필요한 매개변수를 선택적으로 설정할 수 있게 된다.

이는 특히 매개변수가 많은 경우에 유용하다.
또한, 각 매개변수를 어떤 순서로 설정하든 상관없다는 장점도 있다.

</aside>

## 등장 배경

하나의 클래스에 들어가는 인자가 많다면 그만큼 생성자를 많이 만들어야 한다. 

또한, 인자에 대한 설명이 없어 인자가 많은 경우에는 몇 번째 인자가 어떤 인자에 맞는 건지 헷갈릴 수 있다.

```java
public Test {

	private String arg1;
	private String arg2;
	private String arg3;
	// ...

	public Test() {}

	public Test(String arg1) {
		this.arg1 = arg1;
	}

public Test(String arg1, String arg2, ...) {
		this.arg1 = arg1;
		this.arg2 = arg2;
		// ... 생성자를 몇개나 만들어야 하는거야!!
	}
}
```

## Ex. Builder Patten Code

```java
public class Pizza {
    private String dough = "";
    private String cheese = "";
    private String topping = "";

    public static class PizzaBuilder {
        private String dough;
        private String cheese;
        private String topping;

        public PizzaBuilder dough(String dough) {
            this.dough = dough;
            return this;
        }

        public PizzaBuilder cheese(String cheese) {
            this.cheese = cheese;
            return this;
        }

        public PizzaBuilder topping(String topping) {
            this.topping = topping;
            return this;
        }

        public Pizza build() {
            return new Pizza(this);
        }
    }

    private Pizza(PizzaBuilder builder) {
        dough = builder.dough;
        cheese = builder.cheese;
        topping = builder.topping;
    }

    // getters and toString()...
}
```

```java
Pizza pizza1 = new Pizza.PizzaBuilder()
    .dough("wheat")
    .cheese("mozzarella")
    .topping("mushrooms")
    .build();

Pizza pizza2 = new Pizza.PizzaBuilder()
    .dough("wheat")
    .topping("cheeze")
    .build();
```

위와 같이 Builder Pattern을 구현하면 인자의 상관없이 인스턴스를 생성할 수 있다.