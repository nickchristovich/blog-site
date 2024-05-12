---
layout: post
title: Site Overview
date: 2024-05-12 12:00:00 -0400
categories: playground
custom_excerpt: This is my personal site, where I post updates on personal projects and maybe some bloggy type stuff too. This page outlines the decision making process I went through to arrive here. It's also a practice post to get used to my workflow.
---

### TL:DR

This is my personal site, where I post updates on personal projects and maybe some bloggy type stuff too. This page outlines the decision making process I went through to arrive here. It's also a practice post to get used to my workflow.

## Objectives

There were a few factors that led me to this current implementation.

#### Easy to Update

Knowing myself, I would never write anything on this site with any sort of regularity if it required significant effort. I want the site to be a quick place to throw thoughts and updates, not a large tech project in and of itself. This also means finding something with good documentation and support resources.

#### Flexible

As you can probably tell, I'm still not really sure how this site should look or be formatted. I wanted a solution that would be quick to rearrange and redesign if the need arises. I also wanted the option to hit the eject button and leave with all my data if I need to change tools.

#### Cost Effective

I'm ok with spending a bit of money on things that matter, like hosting the site. I do not want to be locked into a tool that requires a costly monthly subscription with few options to back out if your needs change. Although I see the use case for tools like [WebFlow](https://webflow.com/), my needs are much simpler.


## What I'm Using

With the above constraints in mind, I set out to find tools that were cheap/free, flexible, and easy to modify and update and find help. Simple enough right? 

#### Jekyll

[Jekyll](https://jekyllrb.com/) almost instantly generates a site based off of markdown documents. Each doc represents a page or a post, and you can organize them by adding tags. Jekyll makes it super easy to add new updates and also redesign page layouts (or just swap to a different template built by someone else). This is really the backbone of the whole thing. It's free, extremely customizable, documented really well, and has great community support. 

#### GitHub

The code and markdown files for the site live in [this GitHub repo](https://github.com/nickchristovich/blog-site). 

#### Netlify

I am using [Netlify](https://www.netlify.com/) to deploy the site. Netlify was a good solution for me because it is pretty hands-off once you get it set up. Any time I push an update to the GitHub repo, Netlify automatically rebuilds and deploys the site to reflect those changes. I just need to keep in mind that I am on the free plan which includes only 300 build minutes and 100GB of bandwidth each month. So if I find myself updated the site more frequently, or if I suddenly become much more popular, I might have to start paying or look for an alternative.

## Resources

I used the following resources while setting up the site:

- [Jekyll Docs](https://jekyllrb.com/docs/)
- [Netlify Jekyll Tutorial](https://www.netlify.com/blog/2020/04/02/a-step-by-step-guide-jekyll-4.0-on-netlify/)
- [Guy Pursey Jekyll Workflow](https://guypursey.com/blog/201606131900-from-idea-to-published-post-workflow-using-jekyll)