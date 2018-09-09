---
title: "Cleaner React with Class Fields."
date: 2018-09-04T20:12:09+05:30
draft: false
---

Now, write class methods that are <i>automatically bound</i> to the class instance without any overhead syntax.

This is possible because of this ECMAScript [proposal](https://github.com/tc39/proposal-class-fields).

![Example 1](/images/cleaner1.png)

And here's the [fiddle](https://jsfiddle.net/8ja6erbk/7/). 

As you can see it eliminates the need for a `this.doWork = this.doWork.bind(this)` in the `constructor` and we can also avoid creating a new fat arrow function <br />
like so `<button onClick={() => this.doWork()}>` inside each render cycle.

<br />
#### What if the method takes an argument and is called with an item from an array? 


No worries! Instead of <i>doing work</i>, just make the original return another arrow function and do the actual work inside the returned function. The returned function will have access to the original argument via the power of closure.

![Example 2](/images/cleaner2.png)

And here's the [fiddle](https://jsfiddle.net/8ja6erbk/22/).

Cheers!

<i>"Making the simple complicated is commonplace; making the complicated simple, awesomely simple, that's creativity."</i>
Charles Mingus.

<br />
Clap for this article on [medium](https://medium.com/@mustansirzia/cleaner-react-with-class-fields-8e33e7d8dd25)?