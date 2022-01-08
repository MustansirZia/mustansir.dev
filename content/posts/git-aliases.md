---
title: "Git Aliases that Save Time."
date: 2020-05-09T01:12:00+05:30
draft: false
---

For quite some time now I've been using certain aliases in my terminal that make my git workflow go faster. 
Well, git commands aren't really that long but when you only need to type <b>two letters</b>, ↵ and that's enough to 🚀.

<i>Your lazy self cannot thank you enough.</i>

First, a few items in the bash file. <br />
(If you’re using a different shell than bash then the filename and directory might differ)
![Your Bash File](/images/git_aliases.png)

Then, it's showtime in the repo. 
![Your Terminal](/images/git_aliases_2.png)

Couldn't have pushed out a feature sooner. :)

Also, do note these aliases are somewhat generic. Means even though the remote defaults to the origin different remotes can still be specified. For example `$ gp heroku master` where the syntax is `$ gp <remote> <branch>`. This works for a different branch in the same origin as well. Say you're on a local master branch, to push up commits to a remote `develop` branch in the origin you could say `$ gp origin master:develop`. 

<br/> 

### Clap for this article on Medium?
https://medium.com/@mustansirzia/git-aliases-that-save-time-bc6386bd7d8e





