---
title: "Ship a Next.js App with a CI/CD Pipeline."
date: 2022-01-08T14:43:00+05:30
draft: false
---

> *This article is a follow up to a live stream that I recorded in 2 parts. In this live stream we did the following:*

• We shipped a small [Next.js](https://nextjs.org) Single Page App to a digital ocean droplet running Ubuntu. We did this without any third party service by using a conventional web server called [nginx](https://www.nginx.com).

• Along the way, we also built a CI/CD pipeline for this right inside GitHub using [GitHub Actions](https://github.com/features/actions). This allowed us to automate running tests and also automate deployments to our web server upon each commit. <br /> *What's a CI/CD Pipeline? Read from [here](https://semaphoreci.com/blog/cicd-pipeline).*

#### Bonus Points.  
• Completely written in [TypeScript](https://www.typescriptlang.org).

• Integration tests written using a headless browser and [cypress](https://www.cypress.io).

• The app used [React Query](https://react-query.tanstack.com) to fetch data from the API.

<br />

### Part 1 - Building the App & Writing Tests.
<iframe width="100%" height="400" src="https://www.youtube.com/embed/hJ94ozgji7o" title="Part 1" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<br />
<br />

### Part 2 - Building the Pipeline on GitHub Actions.
<iframe width="100%" height="400" src="https://www.youtube.com/embed/iehGn1HpBy0" title="Part 2" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<br />
<br />

#### Please subscribe to my YouTube channel as I plan to do more of such recordings.
https://tinyurl.com/465stypj

#### All the code for this project lives on this open source repository.
https://github.com/MustansirZia/institutions-lookup

#### Clap for this article on Medium?
https://medium.com/@mustansirzia/ship-a-next-js-app-with-a-ci-cd-pipeline-56f5050d2001

<br />

## References:
* Institutions API GitHub Repository (https://github.com/MustansirZia/institutions-api)
* Next.js (https://nextjs.org)
* nginx (https://www.nginx.com)
* GitHub Actions (https://github.com/features/actions)
* Cypress (https://www.cypress.io)
* React Query (https://react-query.tanstack.com)
* TypeScript (https://www.typescriptlang.org)