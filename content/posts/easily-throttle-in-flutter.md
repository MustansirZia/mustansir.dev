---
title: "Easily Throttle Functions in Flutter."
date: 2019-10-14T13:53:14+05:30
draft: false
---

### <p>An easy way to throttle any function in Flutter.</p>

So, what is Throttling?

> <i>In software, a throttling process, or a throttling controller as it is sometimes called, is a process responsible for regulating the rate at which application processing is conducted, either statically or dynamically.</i> - Wikipedia

<br />

In scenarios where user interaction takes place there is one kind of problem that we often find ourselves battling with. The problem of a user interacting with our UI too quickly and us not being able to handle it.

Let's conside an example. Suppose there's a button which when tapped calls an API to fetch data. Now, a user may tap on the button repeatedly in a very short span of time. This will result in too many calls to the API. What's worse is that these calls will take up all the available bandwidth or even in some cases the available memory which in turn could stall the user's mobile device or browser. 

The solution? To filter out the interactions based on time. Or in other words, only process one user interaction for a particular period of time and ignore the rest. That's what throttling means for us in mobile or web development.

![Throtte function](/images/throttle_3.gif)

Let's now see an easy way to do this in Dart & Flutter.
<br />
<i>(This example uses [RxDart](https://github.com/ReactiveX/rxdart) and recommends some level of familiarity with RxDart or [ReactiveX](http://reactivex.io) patterns)</i>

• First we define a `throttle` function.

![Throtte function](/images/throttle_1.png)
The `throttle` function returns a throttled version of the function we passed to it.

• And thats it. Let's now use it.

![Usage for throtte function](/images/throttle_2.png)

As you can see, the throttled function `throttledOnClick` is called thrice one after the other and "I'm throttled" is printed only once per 500 milliseconds signalling its correct behaviour.