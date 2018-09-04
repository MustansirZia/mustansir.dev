---
title: "Cleaner React with Class Fields."
date: 2018-09-04T20:12:09+05:30
draft: false
---

Now, write class methods that are <i>automatically bound</i> to the class instance without any overhead syntax.

This is possible because of this ECMAScript [proposal](https://github.com/tc39/proposal-class-fields).

![Example 1](/images/cleaner1.png)

And here's the [fiddle](https://jsfiddle.net/8ja6erbk/7/). 

As you can see if eliminates the need for a `this.doWork = this.doWork.bind(this)` in the `constructor` and we can also avoid creating a new fat arrow function <br />
like so `<button onClick={() => this.doWork()}>` inside each render cycle.

<br />
#### What if the method takes an argument and is called with an item from an array? 


Well, we can map and transform the array into an array of functions using map just like we transform it into JSX inside `render`.
We can then call each corresponding function from the function array in our `render` method.

![Example 2](/images/cleaner2.png)

And here's the [fiddle](https://jsfiddle.net/8ja6erbk/14/).

<i>Caution - If you forget to update your `funcArray` when the `array` inside your state changes, bad things might happen.</i>

Cheers!

<br />
Clap for this article on [medium](https://medium.com/@mustansirzia/cleaner-react-with-class-fields-8e33e7d8dd25)?