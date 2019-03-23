---
title: "Deploy static web applications to S3 and serve them using CloudFront and HTTPS."
date: 2019-03-24T01:30:59+05:30
draft: false
---

### <p>A video tutorial on how to deploy web applications to production on [Amazon S3](https://aws.amazon.com/s3) and server them using a low latency CDN, [CloudFront](https://aws.amazon.com/cloudfront). </p>
It also includes serving the same application over HTTPS using a custom domain name via [Route 53](https://aws.amazon.com/route53) with the help of a free SSL certificate generated from [Amazon Certificate Manager](https://aws.amazon.com/certificate-manager/).

Sounds overwhelming? Not to worry! I've got a whole video in order to explain every step bit by bit. 

The video is divided into two parts. The first part (the longer part) goes around teaching the necessary steps for deployment and works for any web app in general. This should ideally be enough if you're not using a front end framework such as React.js or Vue.js. The second part adds a few more instructions if you're using a front end framework.

So let's not waste time and get right to it. 

<br />

### Part - I
Deploy static web apps to S3 and serve them using CloudFront and HTTPS.

<iframe width="100%" height="400" src="https://www.youtube.com/embed/30cvkLItP58" frameborder="0" allowfullscreen></iframe>

### Part - II 
A few more instructions for SPAs. <br/> <span style="font-size:13px">(Please note if you're using Gatsby.js, these instructions are not applicable)</span>

<iframe width="100%" height="400" src="https://www.youtube.com/embed/Zjj0QFmjTxE" frameborder="0" allowfullscreen></iframe>

<br />
After configuring everything as shown in the video, your next deployment should be as simple as running a single CLI command!

### Pro tip:
In the behaviour settings for CloudFront, change the <b>Object Caching</b> option to <b>Customize</b> and set the <b>Minimum TTL</b>, <b>Default TTL</b> and <b>Maximum TTL</b> to <b>31557600</b>. This ensures the content from your S3 bucket stays inside the CloudFront cache for as long as it can before we invalidate it manually on the next update to our bucket. You'd want this as serving from CloudFront is very much cheaper and also way better performance wise.

> I forgot to mention this in the video. :)

<br />

### Side info: 
The publish script that we use looks like this.

![Publish Script](/images/s3.png)
This script ensures our deploys to S3 with CloudFront are always a one-liner like so
<br /> `yarn publishToS3` or `npm run publishToS3`. <br/> This saves times and is very CI friendly. The <b>aws-cli</b> for running the aws commands can be downloaded from [here](https://aws.amazon.com/cli/).

Also,

> Since our repositories are always private, instead of saving the aws credentials inside the environment we prefer to save them inside this very script and apply them just before we deploy our apps. (notice the `export AWS_**` variables?) This enables everyone on the team to be able to deploy the apps when needed. 
Learn how to get your keys from [here](https://aws.amazon.com/blogs/security/wheres-my-secret-access-key/).

<br /> 

I really hope you've enjoyed the video and it helps you with your next big project! 

Cheers.
