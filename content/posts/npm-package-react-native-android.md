---
title: "What a React Native library with native Android code looks like."
date: 2019-06-16T16:42:00+05:30
draft: false
---

### <p> Package structure (boilerplate) for a react native library containing native Android code. </p>

If you've ever wondered what a react-native library with native Android code looks like, you've come to the right place. This post highlights the things you need to make one and how the folders generally look like.
<br />

Say we're working on an npm package for react native called <b>"react-native-awesomeness"</b> which contains native Android implementation written in Java. Well, this is how the bare bones structure or boilerplate of that package would look like.

<iframe width="100%" height="400" src="https://www.youtube.com/embed/0RjYWGlEVpA" frameborder="0" allowfullscreen></iframe>

<br />
So you'll eventually end up with a structure like this. 

![Initial Structure](/images/react-native-package1.png)

To see what to include in each file, you can take a look at [this](https://github.com/MustansirZia/react-native-fused-location) GitHub repository of a react native package that which provides accurate location updates on Android using its FusedLocation API.

<br />

> <i>If you have the above structure laid down and contents of files are what they should be. This should be enough to make it work for your users and be installable using 
<br /> `npm install react-native-awesomeness` and 
<br /> `react-native link react-native-awesomeness`.</i>

<br />


### Adding the goodies.
Now, at some point you would want users to actually use your package so it's a pretty good idea to add a `README.md` file. The contains of this file appear of the package's npm page and the home page of its GitHub repository. Ideally, this file should contain installation instructions, examples and gif demos (if any). 
<br />
Here's a [good example](https://github.com/MustansirZia/react-native-fused-location/blob/master/README.md) of such a README.md file.
If you plan to support TypeScript, it's also a good idea to make a `index.d.ts` file that will house type definitions for your package. 

The final structure of the package would now look like.
![Final Structure](/images/react-native-package2.png)

Well, now you have a decent idea of how a bare bones npm package for an android react-native package would look like. Do not hesitate to add more source code files as your package grows along. 
<br /> Also, a whole lot of people would thank you if your package has semantic versioning. Do read about it from [here](https://semver.org/).

Cheers for sticking around! 