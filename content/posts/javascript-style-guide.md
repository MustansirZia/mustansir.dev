---
title: "JavaScript Style Guide."
date: 2017-11-30T01:24:07+05:30
draft: false
---

If you're like me, you earn your bread by writing JavaScript; Sometimes really good JavaScript and sometimes, JavaScript full of <i>codesmell</i>. <br />
Folks, it's about time we make use of something called as a style guide for our JavaScript (and React if you're into React/Vue or other big guns).

But first things first.
<h3>WHY THE HELL DO WE EVEN NEED THIS?</h3>
Well, for the following reasons.

• Your code will look <b>amazing</b> and will be <b>readable</b> by you even years down the line.

• Your code will have very less <b>non idiomatic</b> parts. It'll automatically be somewhat good practice if you follow this style guide. <br />For example, it will highlight an error in your IDE or your favourite text editor if you declared a useless function or a redundant variable. <br /> So by implementing a style guide, your IDE or editor will automatically tell you when you're writing bad JS and not just syntactically wrong JS even before you run a single line of code.

• Two people won't be auto aligning the same file with different formatting so as to form an unending cycle and countless git merge conflict cycles. (Trust me, that's something that has happened to me at my office)<br />

• Chances of <b>messing up</b> while writing code decrease exponentially. <br />

• Trust me, you'll be <b>proud!</b> :)

Ummm alright - <i>But what's a style guide?</i> It's a guide that recommends you on how to format and structure your code. Lint basically means to hint beforehand a bad practice or an error in your code. A style guide in JS can be implemented using [eslint](https://eslint.org/). Eslint is by far the most popular tool for code hinting in JS. (There's JSHint too but it isn't as popular)

In eslint, there is a <b>.eslintrc</b> file we should use. It's basically a `json` file with a fancy name and it lives inside the root folder of our project. <br />(alongside .babelrc and package.json) <br />

 Touch this file and install the following dev packages to set up eslint in your next JS project. <br />

`$ touch .eslintrc` <br />
`$ npm i eslint eslint-{config-airbnb,plugin-import} -D`

If it's React or ReactNative. Add another line. <br />

`$ npm i eslint-{plugin-jsx-a11y,plugin-react} -D`

Let's use an `.eslintrc` file that I generally use which looks like this:
```json
{
  "extends": "airbnb",
  "rules": {
    "arrow-parens": "off",
    "global-require": "off",
    "indent": [
      "error",
      4
    ],
    "no-console": "off",
    "comma-dangle": "off",
    "no-underscore-dangle": "off",
    "func-names": "off",
    "no-use-before-define": "off",
    "react/jsx-indent": [
      "error",
      4
    ],
    "react/jsx-indent-props": [
      "error",
      4
    ],
    "react/jsx-filename-extension": [1, { "extensions":   [".js", ".jsx"] }]
  }
}
```
<br />

<i>Sidenote - There's an alternate way to configure eslint without the .eslintrc file. You can place a key called eslintConfig inside your package.json with a value same as that of the json that's inside your .eslintrc. This will however make your package.json file fat and it comes down to personal preference whichever technique you want to use. If my override rules are short, I prefer the package.json way where as if it's long, I'm quite fine with the addition of the .eslintrc file.</i>

<br />
Now, after this comes the important part.
Making our IDEs or text editors use this style guide and hint changes in our code on the fly inside its own UI.
There're plenty of really good articles on this and I think I can point you to a few. (Skip the parts where they add eslint itself to the project. We've already done that, remember?)

• For Atom - https://hackernoon.com/what-is-eslint-how-do-i-set-it-up-on-atom-70f270f57296. <br />
• For WebStorm - https://www.jetbrains.com/help/webstorm/eslint.html. <br />
• For Sublime - https://github.com/roadhump/SublimeLinter-eslint.

There's [google](http://www.google.com) for others!

<br />
Upon following this article, you and your the whole team (if they weren't grumpy enough to try this at the first place) will commit and write code that is beautifully formatted and according to the same style rules. Moreover, you can configure your IDE or text editor to automatically fix and format your files using the same style guide on every save! Neat huh?

<img src="https://raw.githubusercontent.com/MustansirZia/mustansirzia.com/master/static/images/lint.png"</img>
<br />

<img src="https://raw.githubusercontent.com/MustansirZia/mustansirzia.com/master/static/images/lint_jsx.png"</img>

And profit!

<br />
A full documentation of a very good style guide written by [Airbnb](https://www.airbnb.com/) with what's good and what's bad in JS can be found here. I  use the same guide but with minor changes that I listed above in my `.eslintrc` file.
https://github.com/airbnb/javascript

<br />
Just one or two commands with one extra file. That's all it takes for you to feel proud about your code.

Read this article on [medium](https://medium.com/@mustansirzia/javascript-style-guide-c15d8219cec0)?
